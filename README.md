# site

Site oficial do Neuryx.

**Status:** Planejado

## Propósito

Site estático do Neuryx. Por enquanto contém apenas uma página "em breve" com o
logo, a frase de apresentação e links para o GitHub e para o Lyra OS.

Segue o mesmo stack do site do Lyra OS: **HTML, CSS e JavaScript puros**, sem
framework e sem etapa de build.

## Estrutura

```
site/
├── index.html            # página "em breve"
├── assets/
│   └── neuryx-mark.svg   # cópia do símbolo do repositório brand
└── css/
    └── style.css         # paleta do brand; tema claro e escuro via prefers-color-scheme
```

## Desenvolvimento

Abra `index.html` no navegador ou sirva o diretório localmente:

```bash
python3 -m http.server 8000
```

## Acessibilidade

- `lang="pt-BR"` e texto alternativo no logo.
- Contraste mínimo de 4.5:1 para texto nos dois temas.
- Foco visível nos links.

## Relação com outros repositórios

- [`brand`](https://github.com/neuryx-os/brand): fonte do logo e da paleta. Ao
  atualizar o logo no `brand`, atualize a cópia em `assets/`.
- [`lyra-os-linux/site`](https://github.com/lyra-os-linux/site): site do Lyra OS, mesmo stack.

## Licença

O código do site está sob [GPL-3.0](LICENSE). O logo em `assets/` é marca do
projeto Neuryx e segue a [política de marca](https://github.com/neuryx-os/brand/blob/main/TRADEMARK.md).
