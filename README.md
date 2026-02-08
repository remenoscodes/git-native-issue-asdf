# asdf-git-issue

[git-issue](https://github.com/remenoscodes/git-issue) plugin for the [asdf version manager](https://asdf-vm.com).

Distributed issue tracking system built on Git.

## Install

### Plugin

```bash
asdf plugin add git-issue https://github.com/remenoscodes/asdf-git-issue.git
```

### git-issue

```bash
# Show all installable versions
asdf list-all git-issue

# Install specific version
asdf install git-issue 1.0.1

# Set a version globally
asdf global git-issue 1.0.1

# Set a version for current directory
asdf local git-issue 1.0.1

# Now git-issue commands are available
git-issue version
```

## Dependencies

- `bash`, `curl`, `tar`: generic POSIX utilities
- `git`: required by git-issue itself
- `jq`: required by git-issue for JSON processing

## Configuration

Set `ASDF_GIT_ISSUE_DOWNLOAD_URL` to override the default download URL template.

Default: `https://github.com/remenoscodes/git-issue/releases/download/v{version}/git-issue-v{version}.tar.gz`

## Development

### Testing

```bash
# Test installation locally
asdf plugin test git-issue https://github.com/remenoscodes/asdf-git-issue.git \
  "git-issue version"
```

### Plugin Structure

```
bin/
  download     - Downloads the release tarball
  install      - Installs from downloaded tarball
  list-all     - Lists all available versions
```

## License

GPL-2.0 - Same as git-issue

## Contributing

Contributions welcome! Please open an issue or PR at:
https://github.com/remenoscodes/asdf-git-issue
