# Magento 2 Claude Code Skills Collection

A comprehensive collection of specialized AI skills for Magento 2 development with Claude Code.

## Overview

These skills transform Claude Code into domain-specific experts for various Magento 2 development tasks. Each skill provides deep expertise in its area, following Magento best practices and enterprise standards.

## Installation

### Option 1: Clone into existing Magento 2 project

```bash
# Navigate to your Magento 2 project root
cd /path/to/your/magento2

# Create .claude directory if it doesn't exist
mkdir -p .claude

# Clone skills into .claude/skills
git clone https://github.com/your-username/magento2-claude-skills.git .claude/skills

# Done! Skills are now available
```

### Option 2: Clone and copy

```bash
# Clone repository anywhere
git clone https://github.com/your-username/magento2-claude-skills.git

# Copy to your Magento project
cp -r magento2-claude-skills /path/to/your/magento2/.claude/skills
```

### Option 3: Add as Git submodule (Recommended for teams)

```bash
# Navigate to your Magento 2 project root
cd /path/to/your/magento2

# Add as submodule
git submodule add https://github.com/your-username/magento2-claude-skills.git .claude/skills

# Commit the submodule
git add .gitmodules .claude/skills
git commit -m "Add Claude Code skills as submodule"
```

To update skills later:
```bash
cd .claude/skills && git pull origin main
```

### Verify Installation

```bash
# Check skills directory exists
ls -la .claude/skills/

# You should see directories like:
# alpine-specialist/
# api-developer/
# module-developer/
# ... etc
```

### Start Using

1. Open your Magento 2 project in terminal
2. Run Claude Code: `claude`
3. Use any skill: `/module-developer create a new payment module`

## Quick Start

```bash
# Invoke any skill using slash command
/skill-name

# Or with context
/skill-name your specific question or task
```

## Available Skills

### Backend Development

| Skill | Command | Description |
|-------|---------|-------------|
| Module Developer | `/module-developer` | Create robust, maintainable Magento 2 modules |
| Model Developer | `/model-developer` | Data layer architecture, EAV, repositories |
| API Developer | `/api-developer` | REST & GraphQL API design and implementation |
| Feature Developer | `/feature-developer` | Implement business requirements and features |
| Cronjob Developer | `/cronjob-developer` | Scheduled tasks and background processing |
| PHP Specialist | `/php-specialist` | Advanced PHP techniques and optimization |

### Frontend Development

| Skill | Command | Description |
|-------|---------|-------------|
| Frontend Developer | `/frontend-developer` | Comprehensive frontend solutions |
| Theme Developer | `/theme-developer` | Custom themes and theme modifications |
| Hyva Specialist | `/hyva-specialist` | Hyva theme with Alpine.js & Tailwind |
| Luma Specialist | `/luma-specialist` | Luma theme customization |
| UI Component Developer | `/ui-component-developer` | Admin UI components and grids |
| CSS Specialist | `/css-specialist` | CSS/LESS and responsive design |

### JavaScript Frameworks

| Skill | Command | Description |
|-------|---------|-------------|
| Alpine Specialist | `/alpine-specialist` | Alpine.js for modern frontends |
| Knockout Specialist | `/knockout-specialist` | KnockoutJS MVVM patterns |
| RequireJS Specialist | `/requirejs-specialist` | AMD modules and JS optimization |
| Magewire Specialist | `/magewire-specialist` | Reactive Livewire-style components |

### Configuration & XML

| Skill | Command | Description |
|-------|---------|-------------|
| XML Specialist | `/xml-specialist` | Layout XML, DI, system config |
| Configuration Specialist | `/configuration-specialist` | System settings analysis |

### Performance & Optimization

| Skill | Command | Description |
|-------|---------|-------------|
| Performance Analyst | `/performance-analyst` | Performance analysis and tuning |
| Cache Analyst | `/cache-analyst` | Cache strategy and optimization |
| Index Analyst | `/index-analyst` | Indexing and Elasticsearch optimization |

### DevOps & Infrastructure

| Skill | Command | Description |
|-------|---------|-------------|
| Deployment Engineer | `/deployment-engineer` | CI/CD, Docker, Kubernetes |
| Environment Engineer | `/environment-engineer` | Server setup and optimization |
| Local Environment Specialist | `/local-environment-specialist` | Docker, Valet+, local dev setup |

### Security & Quality

| Skill | Command | Description |
|-------|---------|-------------|
| Security Analyst | `/security-analyst` | Security assessment and hardening |
| Code Reviewer | `/code-reviewer` | Code review and quality assurance |

### Data & Analysis

| Skill | Command | Description |
|-------|---------|-------------|
| Catalog Specialist | `/catalog-specialist` | Catalog data analysis |
| Order Specialist | `/order-specialist` | Order data and transaction analysis |

### Troubleshooting & Migration

| Skill | Command | Description |
|-------|---------|-------------|
| Issue Debugger | `/issue-debugger` | Debug and resolve technical issues |
| Upgrade Specialist | `/upgrade-specialist` | Version upgrades and migrations |

## Skills by Use Case

### "I need to build a new module"
```
/module-developer
```

### "My site is slow"
```
/performance-analyst
```

### "I need to create a REST API"
```
/api-developer
```

### "I'm upgrading to Magento 2.4.7"
```
/upgrade-specialist
```

### "I need to customize the checkout"
```
/frontend-developer
```

### "I'm migrating to Hyva theme"
```
/hyva-specialist
```

### "I need to set up CI/CD"
```
/deployment-engineer
```

### "I have a bug I can't find"
```
/issue-debugger
```

### "I need to optimize database queries"
```
/model-developer
```

### "I need to secure my store"
```
/security-analyst
```

## Directory Structure

```
skills/
├── README.md                      # This file
├── alpine-specialist/
│   └── SKILL.md
├── api-developer/
│   ├── SKILL.md
│   └── README.md
├── cache-analyst/
│   └── SKILL.md
├── catalog-specialist/
│   └── SKILL.md
├── code-reviewer/
│   └── SKILL.md
├── configuration-specialist/
│   └── SKILL.md
├── cronjob-developer/
│   └── SKILL.md
├── css-specialist/
│   └── SKILL.md
├── deployment-engineer/
│   ├── SKILL.md
│   └── README.md
├── environment-engineer/
│   └── SKILL.md
├── feature-developer/
│   └── SKILL.md
├── frontend-developer/
│   └── SKILL.md
├── hyva-specialist/
│   └── SKILL.md
├── index-analyst/
│   └── SKILL.md
├── issue-debugger/
│   └── SKILL.md
├── knockout-specialist/
│   └── SKILL.md
├── local-environment-specialist/
│   └── SKILL.md
├── luma-specialist/
│   └── SKILL.md
├── magewire-specialist/
│   └── SKILL.md
├── model-developer/
│   └── SKILL.md
├── module-developer/
│   └── SKILL.md
├── order-specialist/
│   └── SKILL.md
├── performance-analyst/
│   └── SKILL.md
├── php-specialist/
│   └── SKILL.md
├── requirejs-specialist/
│   └── SKILL.md
├── security-analyst/
│   └── SKILL.md
├── theme-developer/
│   └── SKILL.md
├── ui-component-developer/
│   └── SKILL.md
├── upgrade-specialist/
│   └── SKILL.md
└── xml-specialist/
    └── SKILL.md
```

## Creating Custom Skills

Each skill follows this structure:

```
skill-name/
└── SKILL.md    # Skill definition and instructions
```

### SKILL.md Template

```markdown
You are an expert [specialization] specialist...

## Core Expertise
- Area 1
- Area 2

## Process Framework
1. Step 1
2. Step 2

## Best Practices
- Practice 1
- Practice 2
```

## Requirements

- Claude Code CLI
- Magento 2.4.x project
- Skills directory at `.claude/skills/`

## Contributing

1. Create a new directory for your skill
2. Add `SKILL.md` with comprehensive instructions
3. Optionally add `README.md` for documentation
4. Submit a pull request

## Version Compatibility

| Magento Version | Compatibility |
|-----------------|---------------|
| 2.4.7 | Full |
| 2.4.6 | Full |
| 2.4.5 | Full |
| 2.4.4 | Partial |

## License

MIT License - Feel free to use and modify for your projects.

## Support

For issues or feature requests, please open an issue in the repository.