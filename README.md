# SlyxUp

Modern, security-first CLI for scaffolding projects with production-grade templates and modular features.

## 🚀 Quick Start

```bash
# Install globally
npm install -g slyxup

# Create a new project
slyxup init react my-app

# Add features to existing project
cd my-app
slyxup add tailwind
slyxup add shadcn

# List available options
slyxup list templates
slyxup list features
```

## 📦 Repositories

SlyxUp is organized into multiple repositories:

- **[cli](https://github.com/slyxup/cli)** - Main CLI tool (this is what you install)
- **[registry](https://github.com/slyxup/registry)** - Template and feature registry
- **[templates](https://github.com/slyxup/templates)** - Template source code
- **[features](https://github.com/slyxup/features)** - Feature packages (coming soon)

## 🌟 Features

### Security-First Architecture
- SHA-256 integrity verification for all downloads
- Path traversal protection
- Sandboxed extraction
- Secure dependency management

### Registry-Driven
- All templates and features defined in remote registry
- No hardcoded templates in CLI
- Easy to add new templates without CLI updates
- Version pinning and updates

### Production-Grade
- Transactional operations with automatic rollback
- Comprehensive error handling
- Structured logging
- Smart caching with integrity validation
- Offline mode support

### Developer Experience
- Interactive CLI with helpful prompts
- Clear progress indicators
- Detailed error messages
- Comprehensive documentation

## 📚 Documentation

- **[Deployment Guide](./DEPLOYMENT_GUIDE.md)** - Complete production deployment walkthrough
- **[Project Overview](./PROJECT_OVERVIEW.md)** - Architecture and status
- **[Testing Guide](./TESTING_GUIDE.md)** - Local testing instructions
- **[CLI Documentation](https://github.com/slyxup/cli/blob/main/README.md)** - Command reference

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                   npm install -g slyxup                     │
│                      (CLI Tool)                             │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│              registry.slyxup.online                         │
│          Fetches registry.json with metadata                │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│               cdn.slyxup.online                             │
│      Downloads and verifies template archives               │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│             Your Project Directory                          │
│    Secure extraction, dependency installation               │
└─────────────────────────────────────────────────────────────┘
```

## 🛠️ Available Templates

- **React** - React 18 + Vite + TypeScript
- **Vue** - Vue 3 + Vite + TypeScript (coming soon)
- **Next.js** - Next.js 14 + App Router (coming soon)
- **Express** - Express + TypeScript API (coming soon)

## 🎨 Available Features

- **Tailwind CSS** - Utility-first CSS framework (coming soon)
- **shadcn/ui** - Re-usable components (coming soon)
- **Lucide Icons** - Beautiful icon library (coming soon)
- **Authentication** - Auth setup (coming soon)

## 🚀 Deployment

The project is deployed using:

- **Cloudflare Pages** - Hosts the registry (registry.slyxup.online)
- **Cloudflare R2** - Stores template archives (cdn.slyxup.online)
- **npm** - Distributes the CLI package
- **GitHub** - Source code and version control

All services are on free tier, with zero monthly costs.

## 🧪 Development

### Local Testing

```bash
# Clone the mono-repo
git clone https://github.com/slyxup/slyxup.git
cd slyxup

# Test locally
./test-local.sh

# Or manually:
cd registry && npm run test:local  # Terminal 1
cd cli && npm run build && npm link  # Terminal 2
slyxup init react test-app  # Test command
```

### Contributing

We welcome contributions! Please see the individual repository READMEs for contribution guidelines:

- [CLI Contributing Guide](https://github.com/slyxup/cli/blob/main/CONTRIBUTING.md)
- [Templates Contributing Guide](https://github.com/slyxup/templates/blob/main/README.md)

## 📄 License

MIT License - see individual repositories for details.

## 🤝 Support

- **Issues**: Report bugs at [github.com/slyxup/cli/issues](https://github.com/slyxup/cli/issues)
- **Discussions**: Ask questions at [github.com/slyxup/cli/discussions](https://github.com/slyxup/cli/discussions)
- **Website**: [slyxup.online](https://slyxup.online)

## 🎯 Roadmap

- [x] Core CLI functionality
- [x] React template
- [x] SHA-256 integrity verification
- [x] Transaction/rollback system
- [x] Production deployment infrastructure
- [ ] Vue and Next.js templates
- [ ] Feature packages (Tailwind, shadcn, etc.)
- [ ] GitHub Actions integration
- [ ] Landing page and documentation site
- [ ] Analytics and usage tracking
- [ ] Plugin system for custom templates

---

**Built with ❤️ for developers who value security and simplicity.**
