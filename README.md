# CBMM Protocolos — PWA

App para coleta e organização de protocolos com geração automática de ZIPs.

## Como publicar no GitHub Pages

1. Crie um repositório no GitHub (ex: `cbmm-protocolos`)
2. Faça upload dos 3 arquivos:
   - `index.html`
   - `manifest.json`
   - `sw.js`
3. Vá em **Settings → Pages → Source: main branch / root**
4. Acesse: `https://seu-usuario.github.io/cbmm-protocolos/`

## Ícones (opcional mas recomendado)

Para o banner de instalação nativo funcionar perfeitamente, adicione:
- `icon-192.png` (192×192 px)
- `icon-512.png` (512×512 px)

Use qualquer ferramenta para criar ícones com o logo CBMM.

## Como usar

1. **Abra o app no celular** pelo link do GitHub Pages
2. **Toque em "INSTALAR"** no banner para instalar como app nativo
3. **Configure a API Key** (Anthropic) tocando em "Configurar API Key"
4. **Adicione as fotos** dos protocolos (câmera ou galeria)
5. **Toque em "PROCESSAR COM IA"** — a IA vai:
   - Ler o número do rodapé (ex: 4900231942)
   - Ler o título do cabeçalho (ex: NIQUEL NIOBIO / DELE)
6. **Edite manualmente** se necessário (campos editáveis em cada card)
7. **Toque em "GERAR ZIPS"** — serão gerados:
   - Um ZIP por grupo (ex: `NIQUEL_NIOBIO___DELE.zip`)
   - Cada arquivo dentro nomeado com o número do rodapé (ex: `4900231942.jpg`)

## Tecnologias

- HTML/CSS/JS puro (sem framework)
- PWA com Service Worker (funciona offline após 1ª carga)
- JSZip para geração dos arquivos
- Claude API (claude-opus) para OCR dos protocolos
