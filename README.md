# Fork Setup Tool

A comprehensive tool for setting up GitHub forks with proper configuration, environment verification, and testing.

## Features

- GitHub fork automation
- Go environment verification (1.21+)
- Build and test automation
- Remote configuration management
- Local server verification

## Quick Start

```bash
# Verify Go version
go version

# Install dependencies
go mod download

# Build the project
go build ./...

# Run tests
go test ./...
```

## Repository Setup Steps

1. **Fork on GitHub**
   - Navigate to the original repository
   - Click "Fork" button
   - Select your account as the destination

2. **Clone locally**
   ```bash
   git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
   cd REPO_NAME
   ```

3. **Configure remotes**
   ```bash
   # Add upstream remote
   git remote add upstream https://github.com/ORIGINAL_OWNER/REPO.git
   
   # Verify remotes
   git remote -v
   ```

4. **Verify environment**
   ```bash
   go version  # Should be 1.21 or higher
   ```

5. **Build and test**
   ```bash
   go build ./...
   go test ./...
   ```

## Configuration

Create a `.env` file with your configuration:

```env
GITHUB_TOKEN=your_github_token
UPSTREAM_REPO=original/repo
TARGET_DIR=./projects
```

## Usage

```bash
# Initialize a new fork
./fork-setup-tool init --repo owner/repo

# Verify setup
./fork-setup-tool verify

# Sync with upstream
./fork-setup-tool sync
```

## Success Criteria

- ✅ Clean build (no errors)
- ✅ All tests pass
- ✅ Local server operational
- ✅ Remote configured correctly

## License

MIT
