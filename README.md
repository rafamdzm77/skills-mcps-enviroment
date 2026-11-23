# skills-mcps-enviroment
aqui ficara skills, documentos, mcp para as minhas ias de trabalho 

# RAFA DEV ENVIRONMENT

A personal development environment focused on Full Stack Engineering, Software Architecture, Application Security, and Creative Development.

## About

A modular collection of AI agent skills, shared coding standards, reusable prompts, and PowerShell automation scripts designed to streamline development workflows with OpenAI Codex CLI.

The goal is to establish a consistent, secure, maintainable, and reusable development environment.

## Main Areas

- **Frontend Engineering** — HTML, CSS, JavaScript, TypeScript, React.
- **Backend Engineering** — Node.js, REST APIs, Authentication and Authorization.
- **Database Engineering** — PostgreSQL, MongoDB, SQL and Data Modeling.
- **Application Security** — OWASP, Vulnerability Assessment and Security Auditing.
- **UI/UX Design** — Interface Design, Accessibility and Art Direction.
- **Creative Development** — GSAP, Three.js, WebGL and Interactive Experiences.
- **Code Review** — Architecture, Maintainability, Performance and Quality Assurance.

## Integrations (MCPs)

Documented Model Context Protocol integrations:

- **Context7** — Updated technical documentation.
- **Playwright** — Browser automation and end-to-end testing.
- **GitHub** — Repository, issues and pull request management.

Each integration may require individual installation, authentication or configuration.

## Repository Structure

| Path | Purpose |
|---|---|
| `AGENTS.md` | Project-level engineering and security standards |
| `.agents/skills/` | Specialized agent skills (`SKILL.md`) |
| `config/` | Configuration templates and MCP documentation |
| `prompts/` | Reusable development and review prompts |
| `scripts/` | PowerShell installation and maintenance scripts |
| `docs/` | Installation, configuration and usage guides |

## Prerequisites

- Windows 10/11 with PowerShell.
- Git.
- Node.js and npm.
- OpenAI Codex CLI.

Install Codex CLI:

```powershell
npm install -g @openai/codex
```

## Quick Start

### 1. Clone the repository

```powershell
git clone https://github.com/SEU-USUARIO/rafa-dev-environment.git

cd rafa-dev-environment
```

### 2. Install the environment

```powershell
.\scripts\instalar.ps1
```

### 3. Verify the installation

```powershell
.\scripts\verificar.ps1
```

### 4. Start Codex

```powershell
codex
```

## Skills

The environment includes specialized skills for:

- Frontend Engineering
- Backend Engineering
- Security Audit
- UI/UX Design
- Database Engineering
- GSAP and Three.js
- Code Review

Skills provide specialized instructions and workflows that help Codex perform development tasks consistently.

## MCP Configuration

MCP integrations extend Codex with external tools and resources.

See the MCP documentation:

`config/mcps.md`

Each MCP must be configured and authenticated separately when required.

## Security Guidelines

- Never commit API keys, access tokens or passwords.
- Keep `.env` and credential files out of version control.
- Use environment variables for sensitive information.
- Apply the principle of least privilege.
- Review third-party skills and MCP servers before installation.
- Never execute untrusted scripts without inspecting them.

## Maintenance

Update the local repository:

```powershell
git pull --ff-only
```

Update the installed environment:

```powershell
.\scripts\atualizar.ps1
```

Verify installed components:

```powershell
.\scripts\verificar.ps1
```

## Troubleshooting

If a skill does not appear:

1. Verify that its `SKILL.md` exists.
2. Check its YAML frontmatter.
3. Restart Codex.
4. Verify the installation directory.

If an MCP does not connect:

1. Check the MCP configuration.
2. Verify authentication and environment variables.
3. Check whether the required runtime is installed.
4. Inspect the server error messages.

## License

To be defined.

---

**Built to evolve. Designed for better development workflows.**
