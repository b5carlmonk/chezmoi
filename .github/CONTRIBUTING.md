# Contributing to chezmoi

Thank you for your interest in contributing to chezmoi! This document provides
guidelines and information to help you contribute effectively.

## Code of Conduct

Please read and follow our [Code of Conduct](.github/CODE_OF_CONDUCT.md).

## Getting Started

### Prerequisites

- [Go](https://golang.org/dl/) 1.21 or later
- [Git](https://git-scm.com/)
- Make (optional, but recommended)

### Setting up the development environment

1. Fork the repository on GitHub.
2. Clone your fork locally:
   ```sh
   git clone https://github.com/<your-username>/chezmoi.git
   cd chezmoi
   ```
3. Add the upstream remote:
   ```sh
   git remote add upstream https://github.com/twpayne/chezmoi.git
   ```
4. Install dependencies:
   ```sh
   go mod download
   ```
5. Build the project:
   ```sh
   go build ./...
   ```
6. Run the tests:
   ```sh
   go test ./...
   ```

## Making Changes

### Branching

Create a new branch for each feature or bug fix:

```sh
git checkout -b feat/my-new-feature
```

Use descriptive branch names with a prefix:
- `feat/` for new features
- `fix/` for bug fixes
- `docs/` for documentation changes
- `refactor/` for code refactoring
- `test/` for test additions or modifications

### Coding Standards

- Follow standard Go conventions and idioms.
- Run `golangci-lint` before submitting:
  ```sh
  golangci-lint run
  ```
- Ensure all tests pass:
  ```sh
  go test ./...
  ```
- Add tests for any new functionality.
- Keep commits focused and atomic.

### Commit Messages

We follow the [Conventional Commits](https://www.conventionalcommits.org/)
specification:

```
<type>(<scope>): <short summary>

[optional body]

[optional footer]
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

Examples:
- `feat(cmd): add support for --dry-run flag`
- `fix(template): handle missing variable gracefully`
- `docs: update installation instructions`

## Submitting a Pull Request

1. Push your branch to your fork:
   ```sh
   git push origin feat/my-new-feature
   ```
2. Open a pull request against the `main` branch of this repository.
3. Fill out the pull request template completely.
4. Ensure all CI checks pass.
5. Request a review from a maintainer.

### Pull Request Guidelines

- Keep pull requests focused on a single change.
- Reference any related issues using `Closes #<issue-number>`.
- Update documentation if your change affects user-facing behavior.
- Add or update tests to cover your changes.

## Reporting Issues

When reporting issues, please include:

- chezmoi version (`chezmoi --version`)
- Operating system and version
- Steps to reproduce the issue
- Expected behavior
- Actual behavior
- Any relevant logs or error messages

## Questions

If you have questions, feel free to open a [GitHub Discussion](https://github.com/twpayne/chezmoi/discussions)
or check the [documentation](https://www.chezmoi.io/).
