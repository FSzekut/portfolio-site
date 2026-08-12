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

Qualquer push na `main` publica em produção. Quem faz isso é a integração
nativa do Netlify com o GitHub: uma deploy key de leitura no repositório e um
webhook de push para `api.netlify.com`. Não há GitHub Actions nem token —
o `deploy.yml` foi removido justamente para não disputar o mesmo site.

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
