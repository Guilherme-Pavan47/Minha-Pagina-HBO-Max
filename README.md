# Minha Página HBO Max — Clone Educacional

**Nome:** Guilherme Luiz Pavan Vial
**Matrícula/RA:** 1139397
**Disciplina:** Front-End — Trabalho G1
**Professor:** Matheus Henrique Barquette
**Site de referência:** https://auth.hbomax.com/login

---

## Sobre o projeto

Este repositório contém um clone educacional da tela de login (`/login`) do
HBO Max, desenvolvido apenas com **HTML e CSS**, sem nenhum framework e sem
copiar o código-fonte original — a página foi construída observando o
resultado visual do site de referência.

Não há nenhum vínculo oficial com a HBO ou a Warner Bros. Discovery; o
projeto tem finalidade exclusivamente acadêmica.

---

## Como abrir o projeto

1. Baixe ou clone este repositório.
2. Abra o arquivo `index.html` diretamente no navegador (duplo clique) —
   não é necessário nenhum servidor ou instalação.

---

## Checklist — Parte 1 (Página HTML e CSS)

### 1.1 Estrutura HTML semântica e acessível ✅

- Uso de tags semânticas: `<header>`, `<main>`, `<section>`, `<nav>` e
  `<footer>`, cada uma representando a parte correspondente da página
  (cabeçalho com logo e link de cadastro, conteúdo principal com o
  formulário de login, navegação de links legais e rodapé com redes
  sociais e informações finais).
- Todas as imagens (`<img>`) possuem atributo `alt` descritivo (ex.:
  `alt="HBO Max"`, `alt="YouTube"`, `alt="Chat de ajuda"`).
- O formulário de login é funcional em termos de estrutura HTML: o campo
  de texto possui um `<label for="identificador">` associado via
  `id`/`for`, além de `aria-describedby` apontando para uma dica extra
  (`campo__dica-oculta`) usada só por leitores de tela.

**Análise da página original (referência para este item):**
A tela de login do HBO Max usa `header` (logo + "Cadastre-se agora"),
uma área central de conteúdo com o formulário de e-mail/celular, e um
rodapé com ícones de redes sociais e uma lista de links legais
(Acessibilidade, Política de Privacidade, Termos de Uso etc.). O
formulário original tem só um campo (identificador de e-mail/celular)
com rótulo visível acima do input, exatamente como foi reproduzido aqui.

### 1.2 Fidelidade visual à referência escolhida ✅

- Proporções, espaçamento, cores (fundo escuro em gradiente radial, cartão
  cinza-escuro, texto branco) e tipografia foram reproduzidos o mais
  próximo possível do original.
- Mesma organização geral: cabeçalho → título "Entre" + subtítulo →
  cartão do formulário → bloco "Ainda não tem uma conta?" → link de ajuda
  → rodapé com redes sociais e links legais.

**Diferenças assumidas conscientemente:**
- A fonte oficial do HBO Max é proprietária; foi usada a fonte gratuita
  **Montserrat** (Google Fonts) nos títulos, por ser a que mais se
  aproxima visualmente (traços geométricos e peso bem alto) sem custo de
  licença.
- Pequenos ajustes de espaçamento (padding do cartão, gap entre campo e
  botão) foram calibrados visualmente comparando prints lado a lado até
  ficarem o mais próximos possível do original.

### 1.3 CSS: seletores, box model e variáveis ✅

O arquivo `style.css` usa pelo menos três tipos diferentes de seletor:

- **Seletor de classe:** `.botao`, `.cartao-login`, `.campo`
- **Seletor descendente:** `.campo input`, `.cadastro-info h2`,
  `.rodape__social a`
- **Pseudo-classe:** `:hover` (`.botao--primario:hover`,
  `.topo__cadastro:hover`) e `:focus` (`.campo input:focus`)

Também são usadas variáveis CSS (`:root`) para cores, espaçamentos e
raios de borda, centralizando o "design system" do projeto
(`--cor-fundo`, `--espaco-md`, `--raio-campo`, etc.).

### 1.4 Responsividade: Flexbox, Grid e mobile first ✅

- O CSS foi escrito **mobile first**: o layout base (fora de qualquer
  media query) já funciona corretamente em telas pequenas.
- **Flexbox** é usado para organizar o cabeçalho, o formulário, a lista
  de redes sociais e o rodapé (`display: flex` em `.topo`, `.form-login`,
  `.rodape__social`, `.rodape__links`, entre outros).
- Há duas media queries:
  - `@media (max-width: 767px)` — ajustes finos do botão de chat no
    mobile.
  - `@media (min-width: 768px)` — a principal, que transforma o
    formulário em um cartão com fundo e borda, aumenta o título e reorganiza
    o rodapé em linha, adaptando o layout para telas maiores.
- Layout testado tanto em largura de celular quanto de desktop.

### 1.5 Personalização e originalidade ✅

Foi adicionada, no rodapé, uma seção **"Sobre este projeto"**
(classe `.sobre-clone`) que não existe no site oficial da HBO Max. Nela
constam a identificação do autor (nome e matrícula), o contexto acadêmico
do trabalho e um aviso de que não há vínculo com a HBO/Warner Bros.
Discovery.

---

## Comparação visual — meu site x site original

| Site original (HBO Max) | Meu clone |
|---|---|
| ![Site original](<img width="1888" height="902" alt="image" src="https://github.com/user-attachments/assets/5a42b7f8-6f1f-4358-a2fd-ff1ab06aa737" />
) | ![Meu clone](<img width="1871" height="830" alt="image" src="https://github.com/user-attachments/assets/501e8ffe-a393-406c-8087-aa6a77ed7ef0" />
) |

---

## Tecnologias utilizadas

- HTML5 semântico
- CSS (variáveis, Flexbox, media queries)
- Google Fonts (Montserrat)
