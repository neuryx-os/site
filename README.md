# site

Site oficial do Neuryx.

**Status:** Em desenvolvimento

## Stack

- **HTML, CSS e JavaScript puros**, sem framework, sem bundler e sem etapa de
  build — o mesmo stack do site do Lyra OS. Qualquer hospedagem estática serve,
  com o site servido a partir da raiz.
- **Nenhum JavaScript na v1.** Todas as interações são links e âncoras. Se
  surgir necessidade real, o script fica em `js/main.js`.
- **Fontes auto-hospedadas** em `assets/fonts/` (woff2, subconjunto `latin`).
  Nenhuma requisição a Google Fonts, CDNs ou outros terceiros.

Sem analytics, cookies, rastreadores ou embeds de terceiros.

## Visualizar localmente

Na raiz do repositório:

```bash
python3 -m http.server 8000
```

Depois abra <http://localhost:8000>. O tema escuro é o padrão; o tema claro é
aplicado quando o sistema está configurado com preferência clara.

## Estrutura

```
site/
├── index.html                # página inicial
├── 404.html                  # página não encontrada
├── robots.txt
├── sitemap.xml
├── css/
│   └── style.css             # tokens, tipografia e layout (escuro e claro)
└── assets/
    ├── neuryx-mark.svg       # símbolo para fundo escuro
    ├── favicon.svg
    ├── favicon-32.png
    ├── apple-touch-icon.png  # 180×180
    ├── og-image.png          # 1200×630, Open Graph
    └── fonts/
        ├── space-grotesk-latin-500.woff2
        ├── space-grotesk-latin-600.woff2
        ├── inter-latin-400.woff2
        ├── inter-latin-500.woff2
        ├── inter-latin-600.woff2
        ├── jetbrains-mono-latin-400.woff2
        └── OFL.txt           # licenças SIL OFL 1.1
```

As fontes vêm dos pacotes do Fontsource 5.3.0 (`@fontsource/space-grotesk`,
`@fontsource/inter`, `@fontsource/jetbrains-mono`).

## Pendências

- **Domínio:** definir o domínio e substituir o marcador `[DOMINIO]` em
  `index.html` (canonical e Open Graph), `robots.txt` e `sitemap.xml`.
- **Hospedagem:** escolher onde o site será publicado.
- **Validação W3C:** rodar o validador HTML (`vnu`) em `index.html` e
  `404.html`.

## Relação com outros repositórios

- [`brand`](https://github.com/neuryx-os/brand): fonte do símbolo e da paleta.
  Ao atualizar o logo no `brand`, atualize `assets/`.
- [`lyra-os-linux/site`](https://github.com/lyra-os-linux/site): site do Lyra OS, mesmo stack.

## Licença

- Código do site: [GPL-3.0](LICENSE).
- Fontes: SIL Open Font License 1.1 ([`assets/fonts/OFL.txt`](assets/fonts/OFL.txt)).
- Nome e logo do Neuryx: sujeitos à [política de marca](https://github.com/neuryx-os/brand/blob/main/TRADEMARK.md) do repositório `brand`.
