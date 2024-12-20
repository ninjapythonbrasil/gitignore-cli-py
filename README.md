# gitignore-cli

![PyPI - Version](https://img.shields.io/pypi/v/gitignore-cli-py?color=%23ffd43b)


**gitignore-cli** is a command-line tool that allows you to easily generate `.gitignore` files by selecting from pre-defined templates. It leverages the collection of `.gitignore` templates provided by GitHub and lets you combine multiple templates into a single file.

## Features

- Generate `.gitignore` files from predefined templates.
- Combine multiple templates into a single `.gitignore` file.
- List available templates.
- Autocomplete support for templates (Bash and Zsh).
- Custom header added to the generated `.gitignore` files.

## Installation

To install **gitignore-cli-py**, we recommend using **pipx** to ensure the command is globally accessible and isolated from other Python packages.

### Install pipx (if not already installed)

`pipx` is a tool to install and run Python applications in isolated environments. First, install `pipx` if you haven't already:

```bash
sudo apt install pipx
```

### Install gitignore-cli-py with pipx
Now, use pipx to install gitignore-cli-py globally:

```bash
pipx install gitignore-cli-py
```

This command will make the gitignore-cli command available globally in your terminal.
After installing, ensure that pipx is added to your PATH by running:

```bash
pipx ensurepath
```

### Verifying the Installation
After installation, you can verify that gitignore-cli is working by running:

```bash
gitignore-cli --help
```

This should display the help message for gitignore-cli.

### Autocomplete setup

The CLI also supports autocompletion for templates when using **Bash** or **Zsh**. To enable autocompletion, follow these steps:

#### For Bash:

Run the following command to generate the autocomplete script and add the following line to your `.bashrc` file:
   
```bash
_GITIGNORE_CLI_COMPLETE=bash_source gitignore-cli > ~/.gitignore-cli-complete.sh
echo "source ~/.gitignore-cli-complete.sh" >> ~/.bashrc
source ~/.bashrc
```

#### For Zsh:

Run the following command to generate the autocomplete script and add the following line to your `.zshrc` file:
   
```bash      
_GITIGNORE_CLI_COMPLETE=zsh_source gitignore-cli > ~/.gitignore-cli-complete.sh
echo "source ~/.gitignore-cli-complete.sh" >> ~/.zshrc
source ~/.zshrc
```

## Usage

### 1. Generate a `.gitignore` file

To generate a `.gitignore` file with one or more templates, use the following command:

```bash
gitignore-cli generate <template1> <template2> --output <output_file>
```

For example, to generate a `.gitignore` file that includes the templates for **Python** and **Node.js**, run:

```bash
gitignore-cli generate Python Node --output .gitignore
```

This will create a `.gitignore` file combining the templates for Python and Node.js.

### List available templates

To list all the available templates:

```bash
gitignore-cli list-templates
```

This will output a list of all templates, organized in columns for easier readability.

### 4. Example

```bash
# Generate a .gitignore file for Python and Node.js 
gitignore-cli generate Python Node --output .gitignore
```

## Custom Header

Each generated `.gitignore` file contains a custom header indicating that the file was generated by **gitignore-cli** along with the date and a reference to the repository. Example header:

```bash
# ====================================== 
# .gitignore file generated by gitignore-cli 
# Generated on: 2024-10-07 01:45:23 
# For more information, visit: https://github.com/ninjapythonbrasil/gitignore-cli 
# ======================================
```

## Contributing

We welcome contributions! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a Pull Request.

Please make sure to update tests as appropriate.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

If you have any questions or suggestions, feel free to open an issue or reach out!
