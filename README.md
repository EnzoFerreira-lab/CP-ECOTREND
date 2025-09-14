🌿 EcoTrend — E-commerce Sustentável








EcoTrend é um e-commerce focado em produtos sustentáveis e ecológicos. Objetivo: oferecer uma experiência de compra limpa, acessível e educativa que incentive um estilo de vida mais consciente.

🔎 Visão geral (introdução)

EcoTrend é um projeto front-end construído com React + Vite que implementa funcionalidades interativas essenciais para um e-commerce: listagem dinâmica de produtos a partir de um JSON, filtros, modal de produto, carrinho persistido em localStorage, checkout simulado e UI responsiva com foco em usabilidade e identidade visual ecológica.

O repositório atual contém:

configuração base com Vite;

lint (ESLint) pronta para JavaScript/JSX;

scripts para desenvolvimento, build e deploy em GitHub Pages;

implementação do fluxo de compra no src/App.jsx (fetch de produtos, filtros, carrinho, checkout simulado).

📂 Estrutura do projeto (resumida)
ecotrend/
├─ .gitignore

├─ README.md

├─ index.html

├─ package.json

├─ vite.config.js

├─ public/

│  └─ vite.svg

└─ src/

   ├─ main.jsx
   
   ├─ App.jsx
   
   ├─ App.css
   
   └─ assets/
      ├─ react.svg
      └─ (imagens do produto)

✅ Funcionalidades implementadas (destaques)

Carregamento dinâmico de produtos via fetch() de um JSON público.

Filtros: categoria + range de preço.

Modal de visualização do produto.

Carrinho lateral (sidebar) com persistência em localStorage (eco_cart).

Checkout simulado com validação de campos e feedback de carregamento.

Layout responsivo e identidade visual com paleta “verde / bege / marrom”.

Configuração para deploy em GitHub Pages (gh-pages) e base configurado em vite.config.js.

🧭 Principais arquivos e responsabilidades

src/main.jsx — bootstrap da aplicação (createRoot).

src/App.jsx — componente principal; contém:

useEffect para fetch() do JSON de produtos;

estados: products, cart, filters, selectedProduct, sidebarOpen, checkoutData, etc;

funções: addToCart, removeFromCart, checkout (simulado);

persistência do carrinho em localStorage.

src/App.css — estilos: grid de produtos, modal, carrinho sidebar, tema e animações.

vite.config.js — plugin React + base configurado para GitHub Pages (/CP-ECOTREND/).

package.json — scripts: dev, build, preview, lint, predeploy + deploy (gh-pages).

🛠 Tecnologias

React (JSX)

Vite (bundler / dev server / HMR)

ESLint (regras básicas + react-hooks)

gh-pages (deploy estático para GitHub Pages)

HTML / CSS (responsivo)

LocalStorage, Fetch API (assíncrono), manipulação do DOM via React

📦 Exemplo de products.json (modelo)

Você consome um arquivo JSON público com o formato abaixo. Hospede-o no seu repositório (ex.: public/produtos.json) ou em outro repo e use a URL raw do GitHub.

[
  {
    "id": "p001",
    "name": "Caneca Reutilizável",
    "category": "Cozinha",
    "price": 39.9,
    "image": "https://raw.githubusercontent.com/USER/REPO/main/assets/caneca.jpg",
    "description": "Caneca de cerâmica com acabamento sustentável."
  },
  {
    "id": "p002",
    "name": "Escova de Dente de Bambu",
    "category": "Higiene",
    "price": 12.5,
    "image": "https://raw.githubusercontent.com/USER/REPO/main/assets/escova.jpg",
    "description": "Cabo de bambu biodegradável."
  }
]


Nota: atualize a URL usada em fetch() dentro de App.jsx para apontar para o caminho raw correto (ex.: https://raw.githubusercontent.com/<usuario>/<repo>/main/produtos.json).

⚙️ Como rodar localmente

Clone o repositório:

git clone https://github.com/EnzoFerreira-lab/CP-ECOTREND.git
cd CP-ECOTREND


Instale dependências:

npm install
# ou
yarn


Rodar em modo desenvolvimento (HMR):

npm run dev
# abra http://localhost:5173


Rodar lint:

npm run lint

📦 Build & Deploy (GitHub Pages)

O projeto já contém scripts e ajustes para deploy via gh-pages.

Confirme em package.json o campo "homepage" apontando para:

"homepage": "https://<usuario>.github.io/<nome-do-repo>"


(no seu caso: "https://EnzoFerreira-lab.github.io/CP-ECOTREND")

Em vite.config.js defina:

// base: '/CP-ECOTREND/',
export default defineConfig({
  plugins: [react()],
  base: '/CP-ECOTREND/'
});


Execute:

npm run build
npm run deploy


(o predeploy já chama build se estiver configurado)

Se preferir, crie um workflow do GitHub Actions para rodar build e fazer publish automaticamente após push para main.

🛡 Boas práticas / observações importantes

Validação de input: o checkout atual é simulado. Antes de integrar pagamentos reais, adicione validações server-side.

Segurança: não armazene dados sensíveis em localStorage. Use tokens curtos/segurança adequada no backend.

Performance: otimize imagens (webp), lazy-load para imagens de produtos.

Acessibilidade: garantir labels, aria-*, e navegabilidade por teclado no modal e sidebar.

Testes: adicionar testes unitários (React Testing Library / Vitest) e E2E (Cypress).

🛣 Roadmap (próximos passos sugeridos)

Backend (API RESTful) para persistência de produtos, pedidos e usuários.

Integração com gateway de pagamento (Pix/Cartão) em ambiente seguro.

Painel administrativo para cadastro/edição de produtos.

Autenticação (JWT / OAuth) para contas de usuário.

Upload e CDN para imagens dos produtos.

Pipeline CI (lint → build → test → deploy) via GitHub Actions.

🤝 Contribuição

Quer contribuir? Obrigado! Siga este fluxo:

Fork do repositório.

Crie uma branch com sua feature: git checkout -b feature/minha-feature.

Faça commits pequenos e descritivos.

Abra um Pull Request explicando a mudança.

Responda feedbacks e atualize o PR.

Siga as regras do ESLint e rode npm run lint antes do PR.

📝 Histórico de commits (resumo rápido)

criando pastas — .gitignore, estrutura inicial (Vite + React).

adicionando imagens — assets e imagens de produto.

criando estrutura do site — App.jsx inicial com fetch, cart, filtros, modal e checkout simulado.

ajustando estrutura do site — pequenos fixes e persistência local.

estilizando css — identidade visual (verde/bege/marrom), responsividade.

realizando ajustes — correções em index.html, vite.config.js e package.json (homepage / base).

ajustando falta de imagens — dependências e config gh-pages.

mudando index / atualizando pages — configuração para publicar em GitHub Pages.

📜 Licença

Este projeto está licenciado sob a MIT License — veja o arquivo LICENSE para detalhes.

Contato

Se quiser trocar ideias, abrir issues ou enviar PRs, use a seção de Issues do repositório GitHub.

Projeto executando e desenvolvido por:
Guilherme de Paula: 562471
Enzo Ferreira: 562448
Guilherme Eduardo: 566045
Matheus Gomes: 562277
