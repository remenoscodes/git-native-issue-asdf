# git-native-issue-asdf

[git-native-issue](https://github.com/remenoscodes/git-native-issue) plugin for the [asdf version manager](https://asdf-vm.com).

Distributed issue tracking system built on Git.

## Install

### Plugin

```bash
asdf plugin add git-native-issue https://github.com/remenoscodes/git-native-issue-asdf.git
```

### git-native-issue

```bash
# Show all installable versions
asdf list-all git-native-issue

# Install specific version
asdf install git-native-issue 1.0.1

# Set a version globally
asdf global git-native-issue 1.0.1

# Set a version for current directory
asdf local git-native-issue 1.0.1

# Now git-native-issue commands are available
git-native-issue version
```

## Dependencies

- `bash`, `curl`, `tar`: generic POSIX utilities
- `git`: required by git-native-issue itself
- `jq`: required by git-native-issue for JSON processing

## Configuration

Set `ASDF_GIT_ISSUE_DOWNLOAD_URL` to override the default download URL template.

Default: `https://github.com/remenoscodes/git-native-issue/releases/download/v{version}/git-native-issue-v{version}.tar.gz`

## Development

### Testing

```bash
# Test installation locally
asdf plugin test git-native-issue https://github.com/remenoscodes/git-native-issue-asdf.git \
  "git-native-issue version"
```

### Plugin Structure

```
bin/
  download     - Downloads the release tarball
  install      - Installs from downloaded tarball
  list-all     - Lists all available versions
```

## License

GPL-2.0 - Same as git-native-issue

## Contributing

Contributions welcome! Please open an issue or PR at:
https://github.com/remenoscodes/git-native-issue-asdf
