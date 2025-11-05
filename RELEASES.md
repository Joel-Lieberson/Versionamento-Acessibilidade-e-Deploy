
# Releases e Versionamento Semântico

- **MAJOR**: mudanças incompatíveis (ex.: reestruturação de rotas).
- **MINOR**: novas funcionalidades compatíveis (ex.: novo componente).
- **PATCH**: correções e ajustes compatíveis (ex.: bugfix).

Fluxo sugerido (GitFlow):
1. `feature/*` ➜ `develop`
2. `release/vX.Y.Z` (congelar features, ajustar bugs)
3. merge em `main` e criar tag **vX.Y.Z**
4. abrir `hotfix/*` a partir de `main` quando necessário
