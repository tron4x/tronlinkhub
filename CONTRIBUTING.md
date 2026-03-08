# Contributing to TRON LinkHub

First off, thank you for considering contributing to TRON LinkHub! 🎉

This document provides guidelines and steps for contributing. Following these guidelines helps communicate that you respect the time of the developers managing and developing this open source project.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Pull Request Process](#pull-request-process)
- [Style Guides](#style-guides)
- [Commit Messages](#commit-messages)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## Getting Started

### Issues

- **Bug Reports**: Use the bug report template to create a detailed report
- **Feature Requests**: Use the feature request template to suggest new ideas
- **Questions**: Use GitHub Discussions for questions and support

### Good First Issues

Look for issues labeled `good first issue` - these are great for newcomers!

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates.

When creating a bug report, include:
- Clear and descriptive title
- Steps to reproduce the behavior
- Expected vs actual behavior
- Screenshots if applicable
- Environment details (OS, browser, Docker version, etc.)

### ✨ Suggesting Features

Feature suggestions are tracked as GitHub issues.

When suggesting a feature, include:
- Clear and descriptive title
- Detailed description of the proposed feature
- Explain why this feature would be useful
- Possible implementation approach (optional)

### 🔧 Code Contributions

1. Fork the repository
2. Create a feature branch from `main`
3. Make your changes
4. Write/update tests if applicable
5. Ensure all tests pass
6. Submit a pull request

## Development Setup

### Prerequisites

- Node.js 18+ (LTS recommended)
- npm or yarn
- Docker (optional, for testing containerized builds)

### Local Development

```bash
# Clone your fork
git clone https://github.com/tron4x/tronlinkhub.git
cd tron-linkhub

# Install dependencies
npm install

# Copy environment file
cp .env.example .env.local

# Edit environment variables
# Set at minimum: EDIT_MODE_PASSWORD=your-dev-password

# Start development server
npm run dev
```

### Running Tests

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Run tests with coverage
npm run test:coverage
```

### Building for Production

```bash
# Build the application
npm run build

# Start production server
npm start
```

### Docker Build

```bash
# Build Docker image
docker build -t tronlinkhub:dev .

# Run container
docker run -p 3000:8080 -e EDIT_MODE_PASSWORD=test tronlinkhub:dev
```

## Pull Request Process

1. **Update Documentation**: Update README.md or other docs if needed
2. **Add Tests**: Add tests for new functionality
3. **Follow Style Guide**: Ensure code follows project conventions
4. **Clean Commits**: Squash commits if needed for a clean history
5. **Describe Changes**: Provide a clear PR description

### PR Checklist

- [ ] My code follows the project's style guidelines
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes

## Style Guides

### TypeScript

- Use TypeScript for all new code
- Define types/interfaces for all data structures
- Avoid `any` type - use `unknown` if type is truly unknown
- Use functional components with hooks for React

### Code Formatting

- Use Prettier for code formatting (config in `.prettierrc`)
- Use ESLint for linting (config in `.eslintrc.json`)
- 2 spaces for indentation
- Single quotes for strings
- No semicolons (configured in Prettier)

### File Naming

- React components: `PascalCase.tsx` (e.g., `TileCard.tsx`)
- Hooks: `camelCase.ts` with `use` prefix (e.g., `useCustomTiles.ts`)
- Utilities: `camelCase.ts` (e.g., `sessionStore.ts`)
- API routes: `route.ts` in appropriate directory

### Component Structure

```tsx
// 1. Imports
import { useState } from 'react'
import { SomeIcon } from 'lucide-react'

// 2. Types/Interfaces
interface MyComponentProps {
  title: string
  onAction: () => void
}

// 3. Component
export function MyComponent({ title, onAction }: MyComponentProps) {
  // 3a. Hooks
  const [state, setState] = useState(false)
  
  // 3b. Handlers
  const handleClick = () => {
    onAction()
  }
  
  // 3c. Render
  return (
    <div>
      <h1>{title}</h1>
      <button onClick={handleClick}>Action</button>
    </div>
  )
}
```

## Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

### Format

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

### Types

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, no logic changes)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

### Examples

```bash
feat(auth): add 2FA TOTP support

fix(tiles): prevent drag on mobile touch events

docs(readme): update deployment instructions

refactor(api): simplify session validation logic
```

## Security

If you discover a security vulnerability, please **do NOT** open a public issue.

Instead, email us at: **contact@tron.dev**

We will address security issues promptly and credit reporters appropriately.

## Questions?

Feel free to open a [GitHub Discussion](../../discussions) for questions, ideas, or general feedback.

---

Thank you for contributing! 🙏
