# Ways of Seeing — Portal da Publisher

Landing page e portal da publisher **Ways of Seeing**.

**Site no ar:** <https://ways-of-seeing.github.io>

---

## Identidade visual

A marca é um olho geométrico com um cubo isométrico no lugar da pupila. As três
faces do cubo representam as três frentes do estúdio:

| Face | Cor | Frente |
| :--- | :--- | :--- |
| Topo | Ciano `#2DE1F7` | Ferramentas e SDK |
| Esquerda | Âmbar `#FB923C` | Jogos |
| Direita | Gelo `#F1F5F9` | Labs e experimentos |

As faces são **chapadas, sem gradiente e sem contorno escuro entre elas**. O
chanfro vem de `stroke` da mesma cor do preenchimento com `stroke-linejoin:
round`. Gradiente e contorno escuro eram o que fundia as três faces numa mancha
só abaixo de 48px.

### Qual arquivo usar

O logo tem versões por faixa de tamanho. Usar a errada é o que fazia a marca
virar borrão em ícone pequeno.

| Arquivo | Quando usar |
| :--- | :--- |
| `logo.svg` | Marca principal, **64px ou mais**. Tem placa de fundo e marcas de enquadramento. |
| `logo-compact.svg` | **24–64px**. Traço mais grosso e sem enfeites, para aguentar redução. |
| `logo-mark.svg` | Sobre fundo colorido. Sem placa; o contorno usa `currentColor`. |
| `favicon.svg` | **24px ou menos**. Só o cubo — abaixo desse tamanho o olho não sobrevive. |
| `logo-horizontal.svg` | Lockup para fundo escuro. Tem fundo próprio. |
| `logo-horizontal-light.svg` | Lockup para fundo claro, com texto escuro. |

> O lockup **precisa** de fundo explícito. A primeira versão saiu transparente e
> o texto branco desaparecia sobre qualquer superfície clara.

### PNGs prontos

| Arquivo | Tamanho | Uso |
| :--- | :--- | :--- |
| `avatar.png` | 512×512 | Avatar da organização no GitHub, itch.io |
| `logo-1024.png` | 1024×1024 | Master em alta, lojas e imprensa |
| `logo-compact-256.png` | 256×256 | Ícone médio |
| `apple-touch-icon.png` | 180×180 | Atalho em iOS |
| `favicon-32.png` | 32×32 | Fallback de favicon |
| `logo-horizontal.png` | 1800×440 | Lockup sobre fundo escuro |
| `logo-horizontal-light.png` | 1800×440 | Lockup sobre fundo claro |
| `org-banner.png` | 1280×480 | Banner do perfil da organização e preview social |

### Regenerando os PNGs

Os PNGs saem dos SVGs. **Não use `qlmanage`**: ele renderiza tudo dentro de um
quadrado e distorce qualquer arte que não seja quadrada — foi assim que o banner
anterior virou 1280×1280 com a arte cortada no meio.

Para regerar, rasterize com largura e altura explícitas (por exemplo, abrindo o
SVG num canvas do navegador com `drawImage(img, 0, 0, largura, altura)`).

---

## Publicando

```sh
npm run deploy:pages
```

O script sincroniza `assets/brand/` para `pages/assets/brand/` e envia o
conteúdo de `pages/` para o repositório `ways-of-seeing.github.io`.
