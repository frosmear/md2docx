# md2docx
Python package that converts homework to APA format.  

It's primary purpose is that I can do my CSU homework in simple markdown format, and the convert it to the bloated APA docx format required. 

## Installation

`md2docx` is a command-line application that . The recommended installation method is [pipx](https://pipx.pypa.io/), which installs the application in an isolated Python environment and makes the `md2docx` command available system-wide.

### Install pipx

On Ubuntu:

```bash
sudo apt update
sudo apt install pipx
pipx ensurepath
```

Restart your terminal or reload your shell configuration:

```bash
source ~/.bashrc
```

### Install md2docx

Install directly from GitHub:

```bash
pipx install git+https://github.com/frosmear/md2docx.git
```

Run the converter from your project directory:

```bash
md2docx sample.json
```

The JSON configuration file specifies the Markdown input, DOCX output, and APA formatting options. Relative file paths are resolved from the current working directory. [Here is an example of the JSON format.](sample.json)

The APA reference template is included with the package and used automatically unless a custom template is specified in the JSON configuration.

### Update or Reinstall

To install the latest version from GitHub, uninstall the existing version and reinstall:

```bash
pipx uninstall md2docx
pipx install git+https://github.com/frosmear/md2docx.git
```

This fetches the current repository contents and replaces the installed version.

### Requirements

- Python 3.10 or later
- Pandoc
- pipx
- `python-docx` (installed automatically as a package dependency)

On Ubuntu, install Pandoc with:

```bash
sudo apt install pandoc
```

### Verify Installation

Check the installed version:

```bash
pipx runpip md2docx show md2docx
```

Check that the command is available:

```bash
md2docx --help
```
