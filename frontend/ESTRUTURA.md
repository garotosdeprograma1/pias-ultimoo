# 📁 Estrutura do Frontend - DaFix

## Organização de Pastas

```
frontend/
├── 📄 index.html                 # Página de login/auth (entrada principal)
├── 📄 script.js                  # Scripts globais
├── 📄 style.css                  # Estilos globais
├── 📄 db.js                      # Configuração do banco de dados
├── 📄 servidor-banco.js          # Servidor de banco de dados
├── 📄 ESTRUTURA.md              # Este arquivo
│
├── 📁 assets/                    # Recursos estáticos
│   └── logo.png
│
├── 📁 public/                    # Landing page pública
│   ├── 📄 index.html            # Home pública
│   ├── 📄 landing.html          # Landing page
│   ├── 📄 institucional.html    # Sobre nós
│   ├── 📄 servicos.html         # Serviços
│   ├── 📄 data.json             # Dados de serviços
│   ├── 📄 style.css             # Estilos landing
│   ├── 📄 script.js             # Scripts landing
│   ├── 📄 landing-page.css      # CSS adicional
│   └── 📄 landing-page.js       # JS adicional
│
├── 📁 cliente/                   # Dashboard do cliente
│   ├── 📄 index.html            # Página principal
│   ├── 📄 style.css             # Estilos do cliente
│   └── 📄 script.js             # Scripts do cliente
│
├── 📁 funcionario/               # Dashboard do funcionário
│   ├── 📁 css/
│   │   └── dashboard.css
│   ├── 📁 js/
│   │   ├── funcionario-agenda.js
│   │   ├── funcionario-pedidos.js
│   │   └── funcionario-servicos.js
│   ├── 📄 funcionario-dashboard.html
│   ├── 📄 funcionario-agenda.html
│   ├── 📄 funcionario-pedidos.html
│   └── 📄 funcionario-servicos.html
│
├── 📁 admin/                     # Painel administrativo
│   ├── 📁 css/
│   │   ├── admin.css
│   │   ├── dashboard.css
│   │   ├── relatorios.css
│   │   ├── servicos.css
│   │   └── usuarios.css
│   ├── 📁 js/
│   │   ├── main.js
│   │   ├── dashboard.js
│   │   ├── relatorios.js
│   │   ├── servicos.js
│   │   └── usuarios.js
│   ├── 📄 dashboard.html
│   ├── 📄 relatorios.html
│   ├── 📄 servicos.html
│   └── 📄 usuarios.html
│
├── 📁 suporte/                   # Centro de suporte
│   ├── 📁 css/
│   │   └── suporte.css
│   ├── 📁 js/
│   │   └── suporte.js
│   ├── 📄 index.html
│   └── 📄 contato.html
│
├── 📁 node_modules/             # Dependências (não incluir em git)
├── 📄 package.json
└── 📄 package-lock.json
```

## 📍 Rotas Principais

| Rota | Arquivo | Descrição |
|------|---------|-----------|
| `/` | `index.html` | Login/Autenticação |
| `/public/` | `public/index.html` | Home pública |
| `/landing` | `public/landing.html` | Landing page |
| `/cliente/` | `cliente/index.html` | Dashboard do cliente |
| `/funcionario/` | `funcionario/funcionario-dashboard.html` | Dashboard do funcionário |
| `/admin/` | `admin/dashboard.html` | Painel administrativo |
| `/suporte/` | `suporte/index.html` | Centro de suporte |

## 🔗 Padrão de Links

Todos os arquivos usam caminhos **relativos** para melhor portabilidade:

```html
<!-- Correto ✅ -->
<link rel="stylesheet" href="./style.css">
<link rel="stylesheet" href="./css/admin.css">
<script src="./script.js"></script>
<script src="./js/main.js"></script>
<img src="../assets/logo.png" alt="Logo">

<!-- Incorreto ❌ -->
<link rel="stylesheet" href="/style.css">
<link rel="stylesheet" href="style.css">
<script src="/script.js"></script>
```

## 📋 Checklist de Linkagem

- ✅ Todos os CSS estão em pastas `css/`
- ✅ Todos os JS estão em pastas `js/`
- ✅ Todos os links usam caminhos relativos
- ✅ Imagens referem-se a `../assets/`
- ✅ Cada módulo tem sua própria estrutura

## 🚀 Como Servir

```bash
# Opção 1: Python
python -m http.server 8000

# Opção 2: Node.js (http-server)
npx http-server

# Opção 3: Node.js (express) - Usar servidor-banco.js
node servidor-banco.js
```

## 📝 Notas Importantes

1. **Não servir com `file://`** - Isso causará problemas com CORS
2. **Assets globais** estão em `assets/` na raiz
3. **Banco de dados** está configurado em `db.js`
4. **Server** pode ser iniciado com `servidor-banco.js`

---
*Última atualização: 09/09/2026*
