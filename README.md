# Portal Product Ops & DesignOps — Thayná Bordin

Portal com minhas criações em Product Operations e DesignOps, publicado via GitHub Pages.

## Publicar no GitHub Pages

1. Em **Settings → Pages**, escolha **Deploy from a branch**.
2. Selecione a branch `main` e a pasta `/ (root)`.
3. O site ficará em `https://thaynabordin.github.io/ProductOperations/`.

## Adicionar uma nova criação

1. Coloque o arquivo `.html` na raiz do repositório (ou numa pasta; o nome da pasta vira a categoria do card).
2. Pronto: a página inicial lista automaticamente todos os `.html` do repositório.
   - O título do card vem da tag `<title>` do arquivo.
   - A descrição vem de `<meta name="description" content="...">`.
3. Se quiser controlar título, descrição, categoria ou ordem, adicione o arquivo ao array `CATALOG` no `index.html`:

```js
const CATALOG = [
  { file: "minha-criacao.html", title: "Minha criação", description: "Descrição curta.", tag: "DesignOps" },
];
```

### Link “voltar ao início”

Cole este trecho logo após a abertura do `<body>` de cada criação:

```html
<a href="./" style="position:fixed;top:16px;left:16px;z-index:9999;padding:.6rem 1.1rem;background:#111118;border:1px solid rgba(155,127,212,.3);color:#D4C4F0;font:400 .72rem/1 'DM Sans',system-ui,sans-serif;letter-spacing:.12em;text-transform:uppercase;text-decoration:none">← Voltar ao início</a>
```

(Para arquivos dentro de pastas, use `href="../"`.)
