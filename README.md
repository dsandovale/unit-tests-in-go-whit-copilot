# unit-tests-in-go-whit-copilot

## .devcontainer 

### Concepto general
- .devcontainer es una carpeta de configuración de **Dev Containers** (VS Code Remote Containers / GitHub Codespaces).
- Define entorno reproducible para el proyecto:
  - imagen base (`image`) o Dockerfile.
  - extensiones VS Code.
  - herramientas y features instaladas.
  - usuario remoto, puertos, comandos post-creación.

### Beneficios
- homogeneidad entre desarrolladores
- "works on my machine" mitigado
- integración con CI/CD y Codespaces
- rápido onboarding (no config local larga)

### Implementación actual en tu proyecto

En ` .devcontainer/devcontainer.json` ya está configurado:

1. `name`: `unit-tests-in-go-whit-copilot`
2. `image`: `mcr.microsoft.com/devcontainers/go:2-1.24-bullseye`
3. `features`:
   - `ghcr.io/devcontainers/features/git:1`
   - `ghcr.io/devcontainers/features/github-cli:1`
4. `customizations.vscode.extensions`:
   - `GitHub.vscode-pull-request-github`

### Qué hace esto en concreto
- Instala Go + herramientas esenciales desde imagen oficial.
- Habilita `git` y `gh` en contenedor.
- Añade extensión GitHub para pull requests y flujo GitHub integrado.
