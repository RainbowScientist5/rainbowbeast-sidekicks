Here’s a refreshed and structured version of the README for the **RainbowBeasts Sidekicks** project, designed to be clear, engaging, and contributor-friendly:

---

# 🌈 RainbowBeasts Sidekicks

**Modular Dev Container Templates for Rapid Onboarding and Scalable Development**

Welcome to the RainbowBeasts Sidekicks repository! This toolkit empowers RainbowScientists collaborators to spin up consistent, accessible development environments in seconds—perfect for onboarding, prototyping, and platform component development.

---

## 🚀 What’s Inside

This repo includes two starter templates:

- `hello`: A minimal container for basic setup validation.
- `color`: A customizable container with selectable color themes.

Each template includes:
- `devcontainer-template.json`: Defines metadata and user options.
- `.devcontainer/`: Contains the actual configuration files.
- `test/`: Smoke test scripts for validation.

---

## 🧩 Template Features

Templates support dynamic customization via `devcontainer-template.json`, including:

- **Selectable options** (e.g., favorite color, role type)
- **Semantic versioning** for each template
- **Accessibility toggles** and quickstart scripts (recommended for onboarding flows)

---

## 📦 Publishing to GHCR

Templates are published to **GitHub Container Registry (GHCR)** using the included GitHub Actions workflow:

```bash
ghcr.io/devcontainers/template-starter/color:latest
ghcr.io/devcontainers/template-starter/hello:latest
```

A metadata package is also published for template discovery:
```bash
ghcr.io/devcontainers/template-starter
```

> Distribution spec: [containers.dev implementors guide](https://containers.dev/implementors/templates-distribution/)  
> OCI spec: [opencontainers/distribution-spec](https://github.com/opencontainers/distribution-spec)

---

## 🌍 Make Templates Public

To make your template usable:
1. Go to the GHCR package settings.
2. Set visibility to **public**:
   ```
   https://github.com/users/<owner>/packages/container/<repo>%2F<templateName>/settings
   ```

---

## 📚 Add to the Dev Containers Index

To share your templates with the community:
1. Visit [devcontainers.github.io](https://github.com/devcontainers/devcontainers.github.io)
2. Submit a PR to update [`collection-index.yml`](https://github.com/devcontainers/devcontainers.github.io/blob/gh-pages/_data/collection-index.yml)

This enables visibility in tools like:
- [VS Code Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- [GitHub Codespaces](https://github.com/templates/codespaces)

---

## 🧪 Testing Templates

Use the included GitHub Action workflow and local scripts:

```bash
./.github/actions/smoke-test/build.sh ${TEMPLATE-ID}
./.github/actions/smoke-test/test.sh ${TEMPLATE-ID}
```

Each template has its own `test.sh` in the `test/` folder.

---

## 📝 Auto-Generated Documentation

Documentation for each template is auto-generated from:
- `devcontainer-template.json`
- `NOTES.md`

The GitHub Action in `.github/workflows/release.yaml` handles this automatically.

---

Ready to build your own sidekick? Let me know if you'd like help drafting a new template or expanding this toolkit for your onboarding flows.
