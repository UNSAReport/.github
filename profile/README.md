# UNSAReport Organization

GitHub organization configuration for [UNSAReport](https://github.com/UNSAReport).

## Repositories

| Repository | Description |
|------------|-------------|
| [UNSAReport/UNSAReport](https://github.com/UNSAReport/UNSAReport) | CLI tool for managing lab reports |
| [UNSAReport/templates](https://github.com/UNSAReport/templates) | Typst templates for lab reports |
| [UNSAReport/skills](https://github.com/UNSAReport/skills) | Agent skills for the CLI tool |

## About

UNSAReport is a set of tools for automating reports for the UNSA (Universidad Nacional de San Agustin) Software Engineering career (might look into others depending on success).

### Components

- **CLI Tool** (`unsarep`): Command-line interface for scaffolding, updating, and compiling lab reports
- **Templates**: Typst-based templates for single and multi-lab report structures
- **Skills**: Agent skills compatible with the [vercel-labs/skills](https://github.com/vercel-labs/skills) ecosystem

### Quick Start

```bash
# Install the CLI
go install github.com/UNSAReport/UNSAReport/cmd/unsarep@latest

# Install a template
unsarep install lab

# Edit your report
$EDITOR report.typ

# Prepare submission
unsarep prepare
```

## Contributing

See individual repositories for contribution guidelines.

## License

MIT
