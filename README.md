# Git Visualizer

Terminal-based GitHub  commit activity visualization for the last 6 months across all your Git repositories.

## Build

```bash
go mod init git-visual
go mod tidy
go build -o git-visual .
```

## Usage

```bash
# Add repositories to scan
./git-visual -add "/path/to/your/projects"

# Generate visualization with your Git email
./git-visual -email "your@email.com"
```

Find your Git email: `git config --global user.email`

## Global Install

```bash
sudo cp git-visual /usr/local/bin/
```

Repository paths stored in `~/.gogitlocalstats` 
