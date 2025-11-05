
# Projeto — Entrega I e II (HTML5 + CSS3)

Este projeto reúne a **Entrega I (Fundamentos e Estruturação)** e a **Entrega II (Estilização e Leiautes)**.

## O que foi feito (Entrega II)
- **Design System** com variáveis CSS em `assets/css/tokens.css`: paleta com 8+ cores, tipografia (5+ tamanhos) e espaçamentos modulares (8–64px).
- **CSS Modular**: `base.css`, `layout.css`, `components.css`, `forms.css` e `style.css` (faz `@import` de todos).
- **Leiautes**: grade **12 colunas** com classes utilitárias `.row` e `.col-*`, **CSS Grid** e **Flexbox** em componentes.
- **Breakpoints**: 480, 640, 768, 1024, 1280, 1536px.
- **Navegação**: menu principal com **submenu dropdown** e **menu hambúrguer** para mobile.
- **Componentes**: cards responsivos, botões com estados (hover/focus/active/disabled), formulários estilizados com validação visual, **alerts**, **toasts**, **modal**, **badges**.
- **Acessibilidade**: estrutura semântica, `aria-*`, contraste, foco visível e navegação por teclado.

## Estrutura de Pastas
```
entrega-projeto-html5/
├── index.html
├── projetos.html
├── cadastro.html
└── assets/
    ├── css/
    │   ├── tokens.css
    │   ├── base.css
    │   ├── layout.css
    │   ├── components.css
    │   ├── forms.css
    │   └── style.css
    ├── js/
    │   ├── mask.js
    │   └── app.js
    ├── images/
    │   ├── hero.png
    │   ├── hero.webp
    │   ├── poster.png
    │   ├── aula.png
    │   ├── feira.png
    │   └── tec.png
    └── video/
        └── institucional.mp4 (placeholder)
```

## Validação e Publicação
1. Valide os HTMLs no **W3C Validator**.
2. Publique em um **repositório público** no GitHub. (Opcional: ative GitHub Pages para ver online.)


## Entrega III — Interatividade e Funcionalidades (JavaScript)
- **SPA (Single Page Application)** com **hash routing** (`#/inicio`, `#/projetos`, `#/cadastro`, `#/sucesso`).
- **Sistema de Templates JS** em `assets/js/templates.js`.
- **Validação e Consistência** em `assets/js/validation.js`:
  - E-mail, telefone (10/11 dígitos), **CPF com dígitos verificadores**, CEP (00000-000), data de nascimento (sem futuro e idade mínima 16).
  - Exibição de mensagens de erro por campo + alerta por toast.
- **Armazenamento Local** em `assets/js/storage.js` (cadastros salvos no `localStorage` do navegador).
- **Código Modular** em `assets/js/` (router, templates, validation, storage, main).
- **Como usar**: abra `index.html`; a navegação usa `#` (hash) e o formulário salva dados localmente e redireciona para a tela de sucesso.


---

## Entrega IV — Versionamento, Acessibilidade e Deploy

### 1) Git/GitHub (GitFlow, commits semânticos e releases)
- **Branches**:
  - `main`: produção (conteúdo de `dist/` é publicado pelo GitHub Pages).
  - `develop`: integração contínua.
  - `feature/*`: novas funcionalidades.
  - `hotfix/*`: correções urgentes em produção.
- **Commits (Conventional Commits)**: `feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `test:`, `build:`, `ci:` etc.
- **Releases Semânticas**: `v1.0.0`, `v1.1.0`, `v1.1.1` (MAJOR.MINOR.PATCH) criadas a partir da `main` (tags anotadas).

### 2) Acessibilidade (WCAG 2.1 AA)
- Navegação por teclado: **skip link** (`Pular para o conteúdo`), foco visível, `aria-expanded` dinâmico em menus, modal acessível.
- Estrutura semântica e rótulos adequados.
- Contraste mínimo garantido no tema padrão; **alto contraste** e **modo escuro** com `data-theme`.
- Leitores de tela: landmarks, `aria-label`, `role`, `aria-live` para toasts.

### 3) Otimização para produção
- **Minificação** automática para **CSS/JS/HTML** gerando a pasta `dist/`.
- **Imagens otimizadas** (PNG/JPG/WEBP) exportadas para `dist/assets/images`.
- **CI/CD**: Workflow em `.github/workflows/deploy.yml` publica `dist/` no **GitHub Pages**.
