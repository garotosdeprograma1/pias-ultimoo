# DaFix — Plataforma de Serviços Residenciais

## Estrutura do Projeto

```
project/
├── backend/
│   ├── server.js          # Servidor Node.js (porta 5000)
│   └── sql/               # Scripts de banco de dados
│       ├── cadastrar.sql
│       ├── consulta.sql
│       └── criar_tabelas.sql
│
├── frontend/
│   ├── index.html          # Página de login/cadastro
│   ├── landing.html        # Landing page
│   ├── style.css           # Estilos do login
│   ├── script.js           # Lógica do login
│   ├── landing-page.css    # Estilos da landing page
│   ├── landing-page.js     # Lógica da landing page
│   ├── data.json           # Dados de config/clientes/funcionários
│   │
│   ├── admin/              # Painel administrativo
│   │   ├── dashboard.html
│   │   ├── relatorios.html
│   │   ├── servicos.html
│   │   ├── usuarios.html
│   │   ├── css/
│   │   └── js/
│   │
│   ├── cliente/            # Área do cliente
│   │   ├── index.html
│   │   ├── scriptcli.js
│   │   └── stylecli.css
│   │
│   ├── funcionario/        # Área do funcionário
│   │   ├── funcionario-dashboard.html
│   │   ├── funcionario-dashboard.css
│   │   ├── funcionario-dashboard.js
│   │   ├── funcionario-pedidos.html
│   │   ├── funcionario-pedidos.js
│   │   ├── funcionario-servicos.html
│   │   ├── funcionario-servicos.js
│   │   ├── funcionario-agenda.html
│   │   └── funcionario-agenda.js
│   │
│   ├── publico/            # Páginas públicas
│   │   ├── home.html
│   │   ├── institucional.html
│   │   ├── servicos.html
│   │   ├── style.css
│   │   ├── script.js
│   │   └── data.json
│   │
│   ├── suporte/            # Central de suporte
│   │   ├── index.html
│   │   ├── contato.html
│   │   ├── suporte.css
│   │   └── suporte.js
│   │
│   └── assets/            # Imagens e mídia
│       └── logo.png
│
├── .gitignore
├── LICENSE
└── package-lock.json
```

## Como executar

```bash
node backend/server.js
```

O servidor roda em `http://localhost:5000/`
