
## 1. Contexto do Projeto

O terceiro setor brasileiro carece de presença digital profissional. Este projeto visa criar uma plataforma de front-end robusta,
acessível e performática que sirva como uma solução de baixo custo para ONGs gerirem a sua presença online, captarem recursos e engajarem voluntários.

## 2. Funcionalidades Implementadas

O projeto está dividido em duas áreas principais:

### Área Pública (SPA)

Uma Single Page Application (SPA) que carrega conteúdo dinamicamente sem recarregar a página, proporcionando uma experiência de utilizador rápida e fluida.

* **Páginas Dinâmicas:** Início, Sobre Nós, Projetos, Voluntariado, Doações, Transparência e Blog.
* **Formulário Interativo:** Página de voluntariado com máscaras de input (CPF, CEP, Telefone), validação visual e integração com a API **ViaCEP** para preenchimento automático de endereço.
* **Notificações:** Feedback visual de sucesso/erro no envio de formulários.
* **Multimédia:** Galeria de projetos em formato de *cards*, vídeo institucional e áudio de depoimentos.
* **Transparência:** Gráficos dinâmicos (Pizza, Linha, Barras) desenhados com a API de **Canvas** do HTML5.

### Painel Administrativo (Protótipo Estático)

Um protótipo visual de um painel de controlo para a gestão da ONG.

* Página de `login.html`.
* `dashboard.html` com métricas e gestão de informações institucionais.
* `admin-projetos.html` para visualização e gestão de projetos.
* `admin-voluntarios.html` para visualização dos cadastros.

## 3. Stack de Tecnologias

* **HTML5 Semântico:** Estrutura acessível e otimizada para SEO.
* **CSS3:**
    * **Design System:** Arquitetura CSS modular (`@import`) com variáveis para cores, tipografia e espaçamento.
    * **Layout:** CSS Grid para o layout principal e Flexbox para componentes.
    * **Responsividade:** Sistema de 12 colunas e 5 breakpoints.
* **JavaScript (ES6+ Modular):**
    * **Arquitetura SPA:** Um *router* customizado (`router.js`) que usa `fetch()` e `history.pushState()` para navegação.
    * **DOM (Manipulação):** Atualização dinâmica do `<main>` e do `<title>`.
    * **Modularidade:** Código organizado por funcionalidade (`ui.js`, `forms.js`, `charts.js`, `router.js`, `main.js`).
    * **Eventos e APIs:** Gestão de eventos, máscaras, `fetch` (ViaCEP).

## 4. Conformidade e Qualidade

### Acessibilidade (WCAG 2.1 Nível AA)
O projeto foi construído com foco total em acessibilidade:

* **Contraste:** A paleta de cores (inclusive no Modo Escuro) garante um contraste mínimo de 4.5:1.
* **Navegação por Teclado:** O site é 100% navegável usando a tecla `Tab`, com indicadores de foco (`:focus-visible`).
* **Modo Escuro:** O site adapta-se automaticamente ao esquema de cores do sistema do utilizador (`prefers-color-scheme`).

### Desempenho
* **Lazy Loading:** Imagens da galeria usam `loading="lazy"`.
* **Formatos Modernos:** A tag `<picture>` é usada para suportar `.webp`.
* **Código Otimizado:** A arquitetura modular permite a minificação eficiente (ver Fase de Produção).

