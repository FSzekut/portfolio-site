# portfolio-site

Fonte da página única publicada em <https://fernando-szekut.netlify.app>.

O site é um HTML autocontido — sem build, sem dependências, sem JavaScript.
Estilos inline no próprio arquivo, tema claro/escuro pelo `prefers-color-scheme`.

## Estrutura

```
public/index.html   o site inteiro
netlify.toml        diz ao Netlify para publicar public/
.github/workflows/  deploy automático a cada push na main
```

## Publicar

Qualquer push na `main` publica em produção. Nada mais é necessário.

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
