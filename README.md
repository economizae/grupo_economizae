# Economizaê — Landing Page de Tráfego Pago (GitHub Pages)

Página oficial de captura de membros para os grupos do **Economizaê | Achadinhos e Ofertas** (WhatsApp VIP e Canal Telegram 24h), pronta para hospedar **100% grátis no GitHub Pages**.

## Estrutura dos arquivos

- `index.html` — Página principal (`/`)
- `whats/index.html` — Rota dedicada `/whats` (ideal para links de anúncios)
- `assets/config.js` — **Arquivo único de configuração** (links do WhatsApp/Telegram, Meta Pixel, Google Analytics 4, TikTok Pixel e exemplos de ofertas)
- `assets/styles.css` — Visual responsivo mobile-first
- `assets/app.js` — Prévia interativa WhatsApp/Telegram, filtro de vitrine, horário ao vivo de Brasília e disparo automático de eventos de conversão (`Lead`)
- `assets/logo-economizae.png`, `assets/favicon.png`, `assets/og-share.png` — Identidade visual oficial e card de compartilhamento

## Como publicar de graça no GitHub Pages (sem precisar instalar nada)

1. Crie uma conta gratuita em **https://github.com** (ou faça login na sua).
2. Clique em **New repository** (Novo repositório):
   - Nome sugerido: `economizae` (ou `ofertas`)
   - Deixe como **Public** (obrigatório no plano grátis do GitHub Pages)
   - Clique em **Create repository**.
3. Na tela seguinte, clique em **uploading an existing file** (ou **Add file → Upload files**).
4. Arraste **todo o conteúdo de dentro da pasta `Site_Landing`** (os arquivos `index.html`, `404.html`, `.nojekyll`, `README.md` e as pastas `assets/` e `whats/`) para o navegador.
5. Clique no botão verde **Commit changes**.
6. Vá em **Settings → Pages**:
   - Em **Source**, escolha **Deploy from a branch**
   - Em **Branch**, selecione `main` e pasta `/ (root)`
   - Clique em **Save**.
7. Em ~1 minuto seu site estará no ar gratuitamente em:
   - `https://SEU_USUARIO.github.io/economizae/`
   - `https://SEU_USUARIO.github.io/economizae/whats/`

## Como ativar Meta Pixel / Google Analytics / TikTok Pixel

Abra o arquivo `assets/config.js` e preencha apenas o ID que você usar:

```js
metaPixelId: "SEU_ID_DO_META_PIXEL",
ga4Id: "G-XXXXXXXXXX",
tiktokPixelId: "",
```

Quando alguém clicar nos botões do WhatsApp ou Telegram, a página já dispara automaticamente:
- **Meta Pixel**: `PageView` + evento `Lead` (informando canal e posição do botão)
- **GA4**: evento `generate_lead`
- **TikTok Pixel**: evento `SubmitForm`

## Quer testar no seu PC antes de subir?

Basta dar duplo clique em `index.html` dentro da pasta `Site_Landing` que ele abre direto no navegador!
