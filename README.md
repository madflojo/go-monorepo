# go-monorepo

A starter template for Go monorepos, including:

- Multi-module repository structure
- Conventional Commit enforcement
- Release Please configuration for module releases
- Useful Makefiles for building, testing, linting, and benchmarking
- Linting and test workflows

## Setup

1. Replace module paths in go.mod files (root and submodules) to your repository path.
2. Update the `COMPONENTS` variable in the root Makefile to include your submodules.
3. Adjust the `packages` section in `.release-please-config.json` to reflect your modules.
4. Update directory paths and commit message prefixes in `.github/dependabot.yml` as needed.
5. Customize `.github/COMMIT_CONVENTION.md` to list your preferred scopes.

## Usage

Run the default tasks (build, test, lint) for all modules:
```shell
make all
```

Run individual tasks:
```shell
# Build all modules
make build

# Run tests with coverage for all modules
make tests

# Lint all modules
make lint

# Format all code
make format

# Run benchmarks for all modules
make benchmarks

# Clean artifacts
make clean
```
