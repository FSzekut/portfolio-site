# portfolio-site

Fonte da página única publicada em <https://fernando-szekut.netlify.app>.

O site é um HTML autocontido — sem build e sem dependências. Estilos inline no
próprio arquivo. O único JavaScript é o scroll reveal, que degrada para
conteúdo visível sem JS ou com `prefers-reduced-motion`.

## Estrutura

```
public/index.html   o site inteiro
netlify.toml        diz ao Netlify para publicar public/
```

## Publicar

Qualquer push na `main` publica em produção, pela integração nativa do Netlify
com o GitHub. Não há GitHub Actions nem token: o `deploy.yml` foi removido para
não disputar o mesmo site.

> **Por que este repositório é público.** O plano Core Starter do Netlify não
> constrói repositório **privado** — o build é recusado com *"Build blocked:
> Unrecognized Git contributor"*, e não há ajuste de commit que resolva. As
> saídas documentadas são pagar o plano, publicar à mão pelo CLI ou tornar o
> repositório público. Como o conteúdo aqui é exatamente o HTML que qualquer
> visitante já baixa do site, público sai de graça.
>
> Repositório com informação que não deva circular volta a ser privado — e
> nesse caso a publicação passa a ser manual, pelo CLI.

Para publicar da máquina, sem passar pelo GitHub:

```bash
netlify deploy --prod --dir=public
```

## Pré-visualizar antes de publicar

```bash
netlify deploy --dir=public          # gera URL de preview, não mexe em produção
```

## Projeto no Netlify

<https://app.netlify.com/projects/fernando-szekut>
