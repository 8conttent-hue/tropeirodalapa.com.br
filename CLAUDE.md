# CLAUDE.md — TROPEIRODALAPA

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** TROPEIRODALAPA
**Nicho:** Viagens e Turismo
**Keywords:** Localizado logo na entrada da cidade da Lapa com todo conforto e
**Paleta de cores:** sunset | **Fonte:** playfair

Localizado logo na entrada da cidade da Lapa, com todo conforto e comodidade, aliada a tranquilidade e contato com a natureza… Com toda estrutura para atender você e seu evento ou palestra… Auditório Sala de Imprensa Salão de Festas Aconchegante sala de café Academia Sauna Organizamos Casamentos, Palestras e eventos em geral, entre em contato…



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-B |
| Hero | Hero-I |
| Features | Features-E |
| About Section | About-I |
| Posts | Posts-B |
| Footer | Footer-J |
| Página Sobre | Sobre-J |
| Página Contato | Contato-J |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
