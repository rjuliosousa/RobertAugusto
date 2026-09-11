# Robert Augusto — pacotes para GitHub

Este projeto contém a landing page pessoal de Robert Augusto e, separadamente, o painel de relatório do Instagram.

## Pacote recomendado para publicar

Use o arquivo `robert-augusto-landing-github-pages.zip`. Ele contém somente o build estático necessário para a landing page. Depois de descompactar, envie **o conteúdo interno do ZIP** para a raiz do repositório que será publicado pelo GitHub Pages. O arquivo `index.html` deve ficar diretamente na raiz do repositório, ao lado da pasta `assets`.

A página principal é a landing page pessoal. O painel do Instagram permanece no projeto original e não deve ser usado como página inicial do GitHub Pages.

## Estrutura do pacote estático

```text
index.html
404.html
assets/
  *.css
  *.js
```

O `404.html` é uma cópia de segurança do `index.html`, útil para hospedagem estática quando uma rota é acessada diretamente.

## Publicação pelo GitHub Pages

Crie ou abra um repositório no GitHub, copie os arquivos do pacote estático para a raiz, faça commit e push. Em **Settings → Pages**, selecione a branch principal e a pasta `/ (root)`. Depois, abra a URL fornecida pelo GitHub.

Se o repositório for de projeto, a URL normalmente seguirá o formato `https://SEU_USUARIO.github.io/NOME_DO_REPOSITORIO/`. O build foi preparado com caminhos relativos para funcionar nesse formato.

## Pacote-fonte

Use `robert-augusto-site-source.zip` caso queira editar a aplicação. Ele contém `client`, `server`, `shared`, configuração do Vite, `package.json`, `pnpm-lock.yaml` e documentação. A pasta `node_modules` não é incluída.

Para rodar localmente:

```bash
pnpm install
pnpm dev
```

Para gerar novamente a versão estática do GitHub Pages:

```bash
pnpm run build:github
```

O resultado será criado em `dist/public`.

## Observação sobre o relatório

O relatório de Instagram continua disponível no projeto Manus em `/relatorio`. A versão estática da landing page é o pacote recomendado para publicação no GitHub. O relatório usa recursos específicos do projeto Manus e, por isso, não faz parte do pacote estático principal da landing page.
