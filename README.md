# VimFuck

VimFuck is a Vim-based Brainfuck parser powered by Vim macros. This project leverages Vim’s robust macro functionality to parse and interpret Brainfuck code, allowing users to execute Brainfuck programs directly within Vim.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Brainfuck is a minimalist, esoteric programming language with only eight commands. VimFuck enables the interpretation of Brainfuck programs using Vim macros, showcasing the power and flexibility of Vim for non-traditional use cases. This project is a fun and unique way to explore both Vim macros and Brainfuck.

## Features

- **Macro-based Parsing**: Uses Vim macros to interpret Brainfuck commands.
- **Interactive Execution**: Run Brainfuck programs directly within the Vim editor.
- **Lightweight and Dependency-Free**: Only requires Vim – no additional plugins or dependencies needed.
- **Configurable**: Customize macros for extended functionality if desired.

## Installation

1. Download vimfuck.vim using one of the following methods:

### For Linux/macOS:

```bash
curl -L https://raw.githubusercontent.com/1611Dhruv/VimFuck/main/vimfuck.vim -o vimfuck.vim
```

### For Windows (PowerShell):

Open PowerShell and run this command:

```powershell
Invoke-WebRequest -Uri https://raw.githubusercontent.com/1611Dhruv/VimFuck/main/vimfuck.vim -OutFile vimfuck.vim
```

2. Open Vim with your brainfuck program loaded and call

```
:source /path/to/vimfuck.vim
```

3. Run VimFuck function to interpret your brainfuck program.

```
:call Vimfuck()
```

## Usage

1. Open Vim and load your Brainfuck program.
2. Trigger the VimFuck macro to start parsing and executing the Brainfuck code.
3. Output will be shown within Vim.

## Examples

Here's a simple "Hello, World!" example in Brainfuck:

```brainfuck
++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.
```

To execute this in Vim:

1. Open the file in Vim.
2. Call the VimFuck macro (instructions for invoking the macro will depend on your configuration).

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve functionality, add new features, or fix bugs.

## License

This project is licensed under the MIT License.
