# Favicon — Famiglia Tegon

Arquivos gerados a partir do logo oficial da marca.

## 1. Onde colocar os arquivos

Copie todos os arquivos desta pasta para a **raiz do site** (mesmo nível de `index.html`):

```
seu-site/
├── index.html
├── quemsomos.html
├── ...
├── favicon.ico              ← raiz do site
├── favicon.svg
├── favicon-16x16.png
├── favicon-32x32.png
├── favicon-48x48.png
├── favicon-96x96.png
├── apple-touch-icon.png
├── icon-192.png
├── icon-512.png
└── site.webmanifest
```

Por que na raiz? Navegadores e buscadores procuram `favicon.ico` automaticamente
em `https://seudominio.com/favicon.ico`. Manter tudo na raiz evita 404s.

## 2. Snippet HTML — adicione ao `<head>` de TODAS as páginas

Cole o bloco abaixo dentro de `<head>`, logo após a tag `<title>`:

```html
<!-- Favicons Famiglia Tegon -->
<link rel="icon" type="image/svg+xml" href="favicon.svg">
<link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png">
<link rel="shortcut icon" href="favicon.ico">
<link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png">
<link rel="manifest" href="site.webmanifest">
<meta name="theme-color" content="#c41212">
```

## 3. O que cada arquivo faz

| Arquivo | Para que serve |
|---|---|
| `favicon.ico` | Fallback universal (browsers antigos, IE) — contém 16/32/48 |
| `favicon.svg` | Browsers modernos (Chrome 80+, Firefox, Safari) — alta qualidade vetorial |
| `favicon-16x16.png` | Tab do browser em telas comuns |
| `favicon-32x32.png` | Tab do browser em telas retina |
| `favicon-48x48.png` | Atalhos de área de trabalho do Windows |
| `favicon-96x96.png` | Telas hi-DPI / Android Chrome |
| `apple-touch-icon.png` | Ícone quando alguém adiciona o site à tela inicial do iPhone/iPad |
| `icon-192.png` | PWA — exibido quando o site é "instalado" |
| `icon-512.png` | PWA — splash screen ao abrir o site instalado |
| `site.webmanifest` | Metadados para "Adicionar à tela inicial" (Android/Chrome) |

## 4. Como testar

1. Faça upload de todos os arquivos para a raiz do site
2. Adicione o snippet HTML em todas as páginas
3. Limpe o cache do navegador (Ctrl+Shift+R no Windows, Cmd+Shift+R no Mac)
4. Recarregue uma página — o ícone deve aparecer na aba

Se quiser testar em vários browsers de uma vez, use:
https://realfavicongenerator.net/favicon_checker
