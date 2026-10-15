# AuthTIKTOK — Ponte de Redirecionamento HTTPS para o ClipForge AI

Esta página estática serve como **Bridge de Redirecionamento HTTPS** para permitir que o TikTok autorize o ClipForge AI rodando localmente no seu computador (`http://localhost:3000`), contornando a exigência do TikTok de uma URL pública com HTTPS.

---

## 🚀 Como Hospedar no GitHub Pages em 1 Minuto

### Opção 1: Via GitHub Desktop ou Git no terminal
1. Crie um novo repositório no seu GitHub chamado `AuthTIKTOK` (público).
2. Suba este arquivo `index.html` para a branch `main`:
   ```bash
   cd "c:\Projetos\AuthTIKTOK"
   git init
   git add index.html
   git commit -m "feat: tiktok oauth bridge"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/AuthTIKTOK.git
   git push -u origin main
   ```
3. No GitHub, vá em **Settings → Pages**:
   - Em **Branch**, selecione `main` e a pasta `/ (root)`.
   - Clique em **Save**.
4. O GitHub gerará a sua URL HTTPS, por exemplo:
   ```
   https://SEU_USUARIO.github.io/AuthTIKTOK/
   ```

---

## ⚙️ Como Configurar no TikTok e no ClipForge AI

1. No **TikTok for Developers** (https://developers.tiktok.com/):
   - No seu App, procure por **Redirect URI**.
   - Insira exatamente a URL gerada pelo GitHub Pages:
     `https://SEU_USUARIO.github.io/AuthTIKTOK/`

2. No **ClipForge AI**:
   - Abra o arquivo `.env` e adicione ou edite:
     ```env
     TIKTOK_REDIRECT_URI=https://SEU_USUARIO.github.io/AuthTIKTOK/
     ```
   - Ou acesse **Configurações → Redes Sociais → TikTok** no ClipForge AI e configure o campo **Redirect URI**.
