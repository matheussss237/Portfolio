# Portfólio — Matheus Henrique

Portfólio pessoal de **Matheus Henrique**, desenvolvedor back-end em formação (Java, Spring Boot, Node.js e Segurança da Informação), de Gama — DF. Estudante do 3º semestre de Engenharia de Software na UniCEPLAC e técnico em Desenvolvimento de Sistemas pelo Senac-DF.

🔗 **Site:** https://matheussss237.github.io/Portfolio/

## Projetos apresentados

| Projeto | Stack |
|---|---|
| [Brasília Participa](https://github.com/matheussss237/Brasilia-Participa) (destaque) | Node.js, Express, MongoDB Atlas, JavaScript, Leaflet |
| [Lumi](https://github.com/matheussss237/lumi) | Java 21, JavaFX, Spring Boot, MongoDB Atlas, Groq, RAG |
| Fato Real (repositório privado) | Angular, TypeScript, Supabase |
| [Padaria API — H2](https://github.com/matheussss237/Padaria_java_H2) e [MongoDB](https://github.com/matheussss237/Padaria_java_mongoDB) | Java 17, Spring Boot, Spring Security, Docker |

## Tecnologias

- HTML, CSS e JavaScript puro, sem frameworks e sem etapa de build
- [GSAP 3.13](https://gsap.com) via CDN, com os plugins:
  - **ScrollTrigger**: animações ligadas à rolagem (iniciar, `scrub`, `pin`)
  - **ScrollSmoother**: rolagem suave
  - **SplitText**: textos animados por letra, palavra e linha
  - **ScrambleText** e **Text**: efeito "hacker" no cargo e digitação no loader
- `clip-path` (estilo [Clippy](https://bennettfeely.com/clippy/)) para revelar o site, a foto, o menu e as telas do projeto
- View Transitions API para a troca de tema em círculo

## Animações

| Onde | O que acontece | Recurso |
|---|---|---|
| Entrada | Terminal digita `java -jar portfolio.jar`, contador 000→100 e cortina com clip-path | `timeline`, TextPlugin, clip-path |
| Hero | Nome surge letra por letra, a foto é revelada e o cargo "embaralha" em loop | SplitText, ScrambleText |
| Hero (scroll) | Nome sobe, foto gira e diminui (parallax) | `scrub` |
| Sobre | As palavras "acendem" conforme a rolagem | SplitText + `scrub` |
| Números | Contadores animados | `snap` |
| Stack | Faixas infinitas que aceleram com a velocidade do scroll | `getVelocity()` |
| Projeto | A seção fica fixa e as telas do sistema trocam com a rolagem | `pin` + `scrub` + clip-path |
| Mais projetos | Cards entram em sequência e as imagens se revelam | `ScrollTrigger.batch`, clip-path |
| Formação | A linha do tempo se desenha | `scrub` |
| Mouse | Cursor personalizado, botões magnéticos, cards 3D | `quickTo` |

Também tem tema claro e escuro (salvo no navegador), menu em tela cheia no celular e suporte a
`prefers-reduced-motion` (quem desativa animações no sistema vê o site sem elas).

## Estrutura

```
index.html
css/style.css
js/main.js
assets/
  img/      foto e prints dos projetos
  icons/    ícones das tecnologias (Devicon)
  cv/       currículo (cv.html + PDF)
```

## Como editar

- **Textos:** estão todos no `index.html`.
- **Cores:** paleta #651424 (vinho), #FFFFFF (branco) e #FF5825 (laranja), em variáveis no topo do `css/style.css` (`:root` é o tema escuro e `[data-theme="light"]` é o claro).
- **Novo projeto:** copie um `<article class="work-card">` da seção "Mais projetos" no `index.html` e coloque a imagem (16:10) em `assets/img/`.
- **Currículo:** edite `assets/cv/cv.html`, abra no navegador, use *Imprimir → Salvar como PDF* (A4, sem margens, com "gráficos de fundo" ligado) e salve por cima de `assets/cv/Matheus-Henrique-CV.pdf`.

## Rodar localmente

Abra o `index.html` no navegador, ou rode `python -m http.server` e acesse `http://localhost:8000`.
