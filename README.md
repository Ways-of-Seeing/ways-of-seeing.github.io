# Ways of Seeing — Portal da Publisher

Landing page e portal da publisher **Ways of Seeing**.

**Site no ar:** <https://ways-of-seeing.github.io>

---

## Identidade Visual (v3 Orbital)

A marca é um **olho cósmico orbital** com um cubo isométrico no lugar da pupila e uma espiral de diafragma óptico interno, sintetizando o nome *Ways of Seeing* (os modos de ver, observar e projetar universos digitais).

| Face / Elemento | Cor / Hex | Papel no Estúdio |
| :--- | :--- | :--- |
| **Fundo Cósmico** | Obsidian Ink `#060914` | Vácuo e tela profunda de contraste |
| **Topo do Cubo** | Lunar `#EDEAE2` | Arquitetura, clareza e reflexão conceitual |
| **Esquerda do Cubo** | Ultraviolet `#6957FF` | Ferramentas, tecnologia central e motores em Rust |
| **Direita do Cubo** | Phosphor `#D8FF47` | Jogos, interatividade e dinamismo de tela |

O contorno orbital externo conecta o Ultravioleta ao Fósforo através de um gradiente linear (`#6957FF` → `#EDEAE2` → `#D8FF47`), mantendo um brilho luminescente consistente tanto em vetores quanto em composições cinematográficas.

### Arquivos Principais (v3)

Os arquivos mestres vivem em `assets/brand/v3/` e são sincronizados para `pages/assets/brand/v3/`:

| Arquivo | Formato | Quando usar |
| :--- | :--- | :--- |
| `master-orbital-mark.png` | PNG (1254×1254) | Arte texturizada cinematográfica para capas e aberturas sobre fundo escuro. |
| `master-orbital-mark-transparent.png` | PNG (1254×1254) | Versão com transparência alfa para composições, overlays e vídeos. |
| `logo-mark.svg` | SVG | Marca orbital vetorial pura, escalável e perfeita para ícones médios e grandes. |
| `logo-lockup-dark.svg` | SVG | Lockup completo com logotipo e tipografia para fundos escuros. |
| `logo-lockup-light.svg` | SVG | Lockup completo para superfícies claras. |
| `github-org-banner.svg` | SVG (1280×480) | Banner vetorial oficial para o perfil do GitHub. |
| `org-banner.png` | PNG (1280×480) | Banner rasterizado de alta fidelidade para o perfil da organização e OpenGraph. |
| `studio-intro.html` | HTML5/Canvas/Audio | Animação cinematográfica de abertura a 60fps com starfield e áudio procedural. |
| `cover-lettered.svg` | SVG (1600×900) | Capa em 16:9 com letreiro e grid para imprensa e lojas. |
| `cover-art-only.svg` | SVG (1600×900) | Capa limpa sem texto. |

---

## Publicando

```bash
npm run deploy:pages
```

O script sincroniza `assets/brand/` para `pages/assets/brand/` e envia o conteúdo de `pages/` para o repositório `ways-of-seeing.github.io`.
