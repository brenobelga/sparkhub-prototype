# SparkHub – Protótipo (GitHub Pages)

Este repositório contém um **protótipo em HTML de página única** do SparkHub, pronto para ser publicado via **GitHub Pages**.

## Publicar pelo navegador (GUI)

1. Crie um novo repositório no GitHub, por exemplo **sparkhub-prototype** (público).
2. Faça *Upload* destes arquivos (conteúdo do ZIP) para a branch **main** (raiz do repositório).
3. Vá em **Settings → Pages**.
   - **Source**: *Deploy from a branch*
   - **Branch**: **main** / **/** (root)
4. Salve. O GitHub vai mostrar a URL do site publicado (ex.: `https://<seu-usuario>.github.io/sparkhub-prototype/`).

> Dica: Se preferir publicar na raiz do seu domínio GitHub Pages, crie um repositório chamado **<seu-usuario>.github.io** e suba estes mesmos arquivos na raiz.

## Publicar via linha de comando (Git)

```bash
# Troque <seu-usuario> e <repo> conforme desejar
git init
git add .
git commit -m "SparkHub prototype"
git branch -M main
git remote add origin https://github.com/<seu-usuario>/<repo>.git
git push -u origin main
# Ative GitHub Pages em Settings → Pages (Deploy from a branch, main / root)
```

## Sobre o protótipo

- **Tecnologias**: React 18 (UMD), ReactDOM, Babel (transforma JSX no navegador), Tailwind (CDN).
- **Single-file**: todo o protótipo está em `index.html` (sem build).
- **Funcionalidades**: 
  - Tema (claro/escuro) persistido em `localStorage` (toggle no menu lateral).
  - Drawer mobile que fecha ao navegar (tap no backdrop ou rota atual).
  - Páginas mescladas (Hub, Criação, Sessão, Resultados, Marketplace).
  - Marketplace com *Destaques* e *Todos* (filtros por tag e busca).
  - Gráfico em **Resultados** com animação (reinicia ao reabrir a aba).
- **Compatibilidade**: funciona online (GitHub Pages) ou localmente (duplo-clique no `index.html`).

## Atualizações
Basta editar `index.html`, *commit* e *push* — o Pages atualiza automaticamente.
