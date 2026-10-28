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
3. Se quiser controlar título, descrição, categoria, ordem ou a versão em inglês, adicione o arquivo ao array `CATALOG` no `index.html`:

```js
const CATALOG = [
  { file: "minha-criacao.html", title: "Minha criação", description: "Descrição curta.", tag: "DesignOps",
    en: { title: "My creation", description: "Short description." } },
];
```

## Layout padrão das criações

Todas as criações seguem o mesmo layout do Guia de Práticas de Produto: cabeçalho fixo com "← Portal" e o seletor PT/EN, menu lateral, conteúdo ocupando a largura da tela e rodapé.

- O Canvas e o DesignOps × Product Ops usam a folha de estilos compartilhada `creations.css`. Uma criação nova pode usar o mesmo arquivo com `<link rel="stylesheet" href="creations.css">`.
- O Guia tem os mesmos estilos dentro do próprio arquivo.

### Idioma

- A página inicial e as criações abrem no idioma de `?lang=pt` ou `?lang=en`.
- Sem esse parâmetro, usam a última escolha salva no navegador e, na primeira visita, o idioma do navegador.
- Os cards da página inicial levam o idioma para a criação, e o "← Portal" de cada criação volta no idioma atual.
