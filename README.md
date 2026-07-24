# Blog do Luis

Blog pessoal, construído com [Hugo](https://gohugo.io/) + tema
[PaperMod](https://github.com/adityatelange/hugo-PaperMod). Código 100% seu, hospedado
no GitHub Pages, sem depender de nenhuma plataforma de blog de terceiros.

## Rodar localmente

```bash
hugo server -D
```

Abre em `http://localhost:1313/blog-do-luis/`. O `-D` também mostra posts com
`draft = true`.

## Escrever um post novo

```bash
hugo new content posts/nome-do-post.md
```

Edite o arquivo gerado em `content/posts/`, mude `draft = true` para `draft = false`
quando quiser publicar, e dê `git push` — o deploy é automático (veja abaixo).

## Deploy

Todo push na branch `main` dispara o workflow em
`.github/workflows/deploy.yml`, que builda o site com Hugo e publica no GitHub Pages.
Não precisa fazer nada manual além do push.

## Monetização (Google AdSense)

O código já está pronto para AdSense, mas **desligado por padrão**
(`params.adsenseEnabled: false` em `hugo.yaml`). Passos manuais, que só o dono da conta
Google pode fazer:

1. Criar conta em [adsense.google.com](https://adsense.google.com) e cadastrar este
   site (leva de alguns dias a algumas semanas para aprovação).
2. Depois de aprovado, o AdSense mostra um **publisher ID** (formato `ca-pub-...` /
   `pub-...`) e o conteúdo exato do `ads.txt`.
3. Em `hugo.yaml`, trocar `adsensePublisherId` pelo ID real e `adsenseEnabled` para
   `true`.
4. Em `static/ads.txt`, substituir o conteúdo pelo que o AdSense indicar.
5. Fazer `git push` — os anúncios entram automaticamente no `<head>` (script do
   AdSense) e em um slot logo abaixo de cada post (`layouts/_partials/ad-unit.html`).

Para adicionar mais slots de anúncio em outros pontos do layout, reutilize o partial:

```
{{ partial "ad-unit.html" (dict "slot" "SEU_SLOT_ID") }}
```

## Domínio próprio

Hoje o site vive em `https://luis-novoa.github.io/blog-do-luis/`. Para usar um domínio
próprio (ex.: `seudominio.com`):

1. Comprar o domínio num registrador (Registro.br, Namecheap, etc — passo manual, tem
   custo).
2. Criar um arquivo `static/CNAME` com o domínio dentro (uma linha, ex.: `blog.seudominio.com`).
3. Apontar o DNS do domínio para o GitHub Pages (registros `A`/`ALIAS`/`CNAME` conforme
   a [documentação do GitHub Pages](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site)).
4. Atualizar `baseURL` em `hugo.yaml` para o novo domínio.

## Estrutura

- `content/posts/` — os posts, em Markdown.
- `layouts/_partials/` — overrides do tema PaperMod (AdSense fica aqui).
- `hugo.yaml` — configuração do site.
- `.github/workflows/deploy.yml` — build e deploy automático.
