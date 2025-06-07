# Git Visual

Terminal-based GitHub-style commit activity visualization for the last 6 months across all your Git repositories.

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

## Example Output

```
         Jan     Feb     Mar     Apr     May     Jun
       -   -   -   -   -   -   -   -   -   -   -   -
 Mon   -   -   2   -   5   -   -   1   -   -   -   -
       -   -   -   -   -   -   -   -   -   -   -   -
 Wed   -   3   -   -   8   -   -   -   -   -   -   -
       -   -   -   -   -   -   -   -   -   -   -   -
 Fri   -   -   -   -   -  12   -   -   -   -   -   -
       -   -   -   -   -   -   -   -   -   -   -   -
```

Colors: Gray (no commits), Light (1-4), Yellow (5-9), Green (10+)

## Global Install

```bash
sudo cp git-visual /usr/local/bin/
```

Repository paths stored in `~/.gogitlocalstats` 