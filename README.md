# Gobrax KPIs Semanais

Sistema de gestão e apresentação de KPIs semanais para o time de Pós-Vendas da Gobrax.

## 🚀 Deploy no GitHub Pages

### 1. Criar repositório

```bash
git init
git add .
git commit -m "feat: initial commit — Gobrax KPIs"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPO.git
git push -u origin main
```

### 2. Ativar GitHub Pages com Actions

No repositório GitHub:
1. Vá em **Settings → Pages**
2. Em **Source**, selecione **GitHub Actions**
3. O workflow `.github/workflows/deploy.yml` já está configurado
4. O deploy acontece automaticamente a cada `push` na branch `main`

Após o deploy, o site estará disponível em:
```
https://SEU_USUARIO.github.io/SEU_REPO/
```

---

## 🗂 Estrutura do projeto

```
gobrax-kpis/
├── index.html              ← HTML principal
├── css/
│   └── style.css           ← Todos os estilos
├── js/
│   ├── data.js             ← Dados iniciais (seed)
│   ├── storage.js          ← Persistência localStorage
│   ├── helpers.js          ← Funções utilitárias
│   ├── auth.js             ← Login / logout
│   ├── export.js           ← Exportação PDF e Excel
│   ├── app.js              ← Navegação, modal, boot
│   └── pages/
│       ├── dashboard.js
│       ├── kpis-semanais.js
│       ├── fill.js
│       ├── metas.js
│       ├── history.js
│       ├── detail.js
│       ├── users.js
│       ├── areas.js
│       ├── kpis-mgmt.js
│       └── settings.js
└── .github/
    └── workflows/
        └── deploy.yml      ← CI/CD automático
```

---

## 👤 Usuários de demonstração

| Perfil       | E-mail                         | Senha  |
|--------------|-------------------------------|--------|
| Diretor      | diretor@gobrax.com.br          | 123456 |
| Gd. Contas   | grandescontas@gobrax.com.br    | 123456 |
| Suprimentos  | suprimentos@gobrax.com.br      | 123456 |
| Suporte      | suporte@gobrax.com.br          | 123456 |
| CS           | cs@gobrax.com.br               | 123456 |
| Melhoria     | melhoria@gobrax.com.br         | 123456 |

---

## 💡 Funcionalidades

- **Dashboard** — visão geral por área com semáforo de status
- **KPIs Semanais** — one-page com todos os indicadores
- **Preencher Semana** — formulário para gerentes enviarem dados
- **Definir Metas** — painel do Diretor para configurar metas
- **Histórico** — todos os relatórios semanais
- **Gerenciar KPIs / Áreas / Usuários** — administração completa
- **Exportar PDF** — impressão otimizada via `window.print()`
- **Exportar Excel** — arquivo `.xlsx` com 3 abas (Resumo, KPIs, Histórico)
- **Persistência localStorage** — dados salvos automaticamente no navegador

---

## 🛠 Desenvolvimento local

Nenhuma dependência de build. Basta abrir o `index.html` num servidor local:

```bash
# Python
python3 -m http.server 8080

# Node
npx serve .
```

Acesse em `http://localhost:8080`.

> **Nota:** Abrir o `index.html` diretamente como `file://` pode bloquear os módulos JS por restrições de CORS em alguns navegadores. Use sempre um servidor local.
