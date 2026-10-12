# 🍺 Bierbox

**Bierbox** é uma plataforma de assinatura de cervejas artesanais desenvolvida como Trabalho de Conclusão de Curso (TCC) de Engenharia de Software. A proposta é aproximar consumidores de cervejarias artesanais, oferecendo uma experiência de descoberta e compra de cervejas por meio de planos de assinatura.

## 📌 Sobre o projeto

A aplicação reúne uma loja virtual e uma área administrativa. Os usuários podem explorar boxes, escolher um plano, gerenciar o carrinho e os endereços de entrega e seguir o fluxo de checkout. A API separada é responsável pelas regras de negócio e pela integração com serviços de apoio.

## ✨ Funcionalidades

### Para clientes
- Visualização e consulta dos boxes disponíveis.
- Fluxo de compra com seleção do plano e quantidade.
- Carrinho de compras.
- Cadastro e gerenciamento de endereços de entrega.
- Cálculo de frete.
- Fluxo de pagamento integrado.
- Área do usuário para consultar perfil e assinaturas.

### Administração
- Área administrativa para gerenciamento da plataforma.
- Visualização de dados e informações relacionadas às vendas e assinaturas.

> A disponibilidade de cada recurso depende da configuração da aplicação e dos serviços externos utilizados.

## 🧰 Tecnologias

### Frontend
- [Next.js 15](https://nextjs.org/) e [React 19](https://react.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS 3](https://tailwindcss.com/)
- [Axios](https://axios-http.com/) para requisições HTTP
- [TanStack Table](https://tanstack.com/table) para tabelas
- [Embla Carousel](https://www.embla-carousel.com/) para carrosséis
- [Recharts](https://recharts.org/) para visualização de dados

### Backend
- [Node.js](https://nodejs.org/) com [Express 5](https://expressjs.com/)
- [PostgreSQL](https://www.postgresql.org/) com o pacote `pg`
- Autenticação baseada em JWT e senhas protegidas com bcrypt
- Integrações de pagamento com Stripe e Mercado Pago
- Cloudinary para armazenamento de mídia
- Nodemailer e SendGrid para recursos de e-mail

## 📁 Estrutura do repositório

```text
Tcc-Bierbox/
├── app/                 # Aplicação frontend Next.js
│   ├── (pages)/         # Páginas da aplicação
│   ├── api/             # Rotas de API do Next.js
│   ├── components/      # Componentes reutilizáveis
│   ├── context/         # Contextos React
│   ├── hooks/           # Hooks personalizados
│   ├── lib/             # Utilitários
│   └── services/        # Serviços e chamadas à API
├── backend/             # API Node.js / Express
│   ├── config/          # Configurações
│   ├── controllers/     # Controladores
│   ├── middleware/      # Middlewares
│   ├── routes/          # Rotas da API
│   └── index.js         # Inicialização do servidor
├── public/              # Arquivos estáticos
├── package.json         # Dependências e scripts do frontend
└── README.md
```

## ⚙️ Pré-requisitos

Antes de começar, instale:
- [Node.js](https://nodejs.org/) (versão compatível com as dependências do projeto).
- npm (incluído com o Node.js).
- Uma instância PostgreSQL configurada para a aplicação.

Para integrações de pagamento, e-mail e armazenamento de imagens, também podem ser necessárias credenciais dos serviços correspondentes.

## 🚀 Como executar

Clone o repositório:

```bash
git clone https://github.com/TenshiFK/Tcc-Bierbox.git
cd Tcc-Bierbox
```

### 1. Configurar o frontend

Na raiz do projeto, instale as dependências:

```bash
npm install
```

Crie um arquivo `.env.local` na raiz e configure as variáveis de ambiente exigidas pela aplicação, como a URL da API. Os nomes exatos devem corresponder aos utilizados nos arquivos de configuração e serviços do projeto.

Inicie o servidor de desenvolvimento:

```bash
npm run dev
```

Acesse [http://localhost:3000](http://localhost:3000).

### 2. Configurar o backend

Em outro terminal, instale as dependências da API:

```bash
cd backend
npm install
```

Configure as variáveis de ambiente em um arquivo `.env` dentro da pasta `backend`. Inclua, conforme necessário, a conexão com o banco de dados (por exemplo, `DATABASE_URL`), a porta e as credenciais dos serviços externos. Não compartilhe esse arquivo nem envie segredos para o Git.

Inicie a API:

```bash
npm start
```

Por padrão, o servidor utiliza a porta `4000` quando nenhuma variável `PORT` é definida. Com a API em execução, a rota raiz responde em [http://localhost:4000](http://localhost:4000).

## 🔐 Variáveis de ambiente e segurança

As credenciais dependem dos recursos habilitados no ambiente, incluindo banco de dados, autenticação, pagamentos, e-mail e armazenamento de imagens. Consulte os arquivos de configuração e integração do projeto para confirmar os nomes necessários.

- Nunca publique chaves secretas, tokens JWT, senhas ou credenciais de serviços.
- Configure URLs e chaves de teste em ambientes locais.
- Para produção, restrinja as origens permitidas pelo CORS e utilize HTTPS.

## 🎓 Contexto acadêmico

Projeto desenvolvido como Trabalho de Conclusão de Curso (TCC) de Engenharia de Software, com foco na criação de uma solução para conectar consumidores a cervejarias artesanais por meio de boxes e assinaturas.

## 👩‍💻 Autoria

Desenvolvido por [TenshiFK](https://github.com/TenshiFK).

---

<p align="center">Feito com 🍺 para valorizar as cervejas artesanais.</p>
