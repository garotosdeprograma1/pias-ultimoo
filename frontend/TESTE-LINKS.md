# 🧪 Teste de Links - Frontend DaFix

## Checklist de Validação

Use este checklist para verificar se todos os links estão funcionando:

### 🏠 Página Principal
- [ ] `http://localhost:8000/` - Carrega com style.css e script.js
- [ ] Logo exibe (../assets/logo.png)
- [ ] Tema toggle funciona
- [ ] Idioma toggle funciona

### 🌐 Seção Pública
- [ ] `http://localhost:8000/public/` - Home pública
- [ ] `http://localhost:8000/public/landing.html` - Landing page
- [ ] `http://localhost:8000/public/institucional.html` - Sobre nós
- [ ] `http://localhost:8000/public/servicos.html` - Serviços

### 👥 Dashboard Cliente
- [ ] `http://localhost:8000/cliente/` - Página do cliente
- [ ] CSS carrega (./style.css)
- [ ] JS executa (./script.js)

### 👨‍💼 Dashboard Funcionário
- [ ] `http://localhost:8000/funcionario/funcionario-dashboard.html`
- [ ] CSS funciona (./css/dashboard.css)
- [ ] JS funciona (./js/funcionario-*.js)

### ⚙️ Admin
- [ ] `http://localhost:8000/admin/dashboard.html`
- [ ] CSS carrega (./css/admin.css, ./css/dashboard.css)
- [ ] JS executa (./js/main.js, ./js/dashboard.js)

### 🆘 Suporte
- [ ] `http://localhost:8000/suporte/`
- [ ] CSS funciona (./css/suporte.css)
- [ ] JS funciona (./js/suporte.js)

---

## Verificação no Console

1. Abra DevTools (F12)
2. Vá para a aba "Console"
3. Procure por erros **404 (Not Found)**
4. Se houver erros, anote o caminho e corrija

### Comando para verificar arquivos faltantes:

```bash
grep -r "href=\|src=" frontend/ --include="*.html" | grep -v "http"
```

---

## Resolução de Problemas

### Erro: "GET /arquivo.css 404"
**Solução:** Verifique se o caminho está relativo (./arquivo.css)

### Erro: "Cannot find module"
**Solução:** Verifique se o JS está na pasta correta (js/)

### Erro: "Images not loading"
**Solução:** Use ../assets/logo.png para referenciar

### Página branca/vazia
**Solução:** Verifique Console (F12) para erros

---

## Atalho Rápido

```bash
# Na pasta frontend/
python -m http.server 8000

# Abrir em outro terminal
firefox http://localhost:8000
# ou
chrome http://localhost:8000
```

---

*Última verificação: 09/09/2026*
