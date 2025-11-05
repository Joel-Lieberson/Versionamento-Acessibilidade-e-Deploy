
# Acessibilidade — WCAG 2.1 AA

## Atendimentos implementados
- **Perceptível**
  - Contraste mínimo 4.5:1 no tema padrão; **tema de alto contraste** disponível.
  - Texto alternativo em imagens (ex.: imagens de projetos e herói).
  - Estrutura semântica e uso de headings hierárquicos (h1, h2, h3).
- **Operável**
  - **Navegação por teclado**: foco visível, **skip link**, menus com `aria-expanded`, modais fecham com clique fora e possuem foco gerenciável.
- **Compreensível**
  - Rótulos associados, instruções nos campos e mensagens de erro claras.
- **Robusto**
  - Atributos `role`/`aria-*` e landmarks (`header`, `main`, `footer`).

## Testes recomendados
- Navegar com `Tab`/`Shift+Tab` em todas as páginas.
- Verificar reader (NVDA/JAWS/VoiceOver).
- Avaliar contraste (WCAG) e temas (dark/high-contrast).
- Validar HTML/CSS/JS e rodar ferramentas como Lighthouse/Axe.
