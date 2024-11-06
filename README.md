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

### Brainfuck Commands

Brainfuck has only eight commands, each of which performs a simple operation. Here's a quick overview of them:

- **`>`**: Move the data pointer to the right (increment the memory cell pointer).
- **`<`**: Move the data pointer to the left (decrement the memory cell pointer).
- **`+`**: Increment the byte at the data pointer (increase the current memory cell by 1).
- **`-`**: Decrement the byte at the data pointer (decrease the current memory cell by 1).
- **`.`**: Output the value at the data pointer as a character (prints the ASCII character of the value).
- **`,`**: Input a character and store it at the data pointer (stores the ASCII value of the input character).
- **`[`**: Jump forward to the command after the matching `]` if the byte at the data pointer is 0.
- **`]`**: Jump back to the command after the matching `[` if the byte at the data pointer is non-zero.

Each of these commands operates on a simple array of memory cells, with the pointer starting at the first cell. These commands provide all the functionality necessary for Turing-complete computation, albeit in a very cryptic and minimalist way!

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

if your brainfuck program is in the same directory as vimfuck.vim.

```
:source vimfuck.vim
```

or if your brainfuck program is in a different directory,

```
:source /path/to/vimfuck.vim
```

3. Run VimFuck function to interpret your brainfuck program.

```
:call Vimfuck()
```

## Usage

1. Once you have loaded the brainfuck program, source vimfuck.vim.
2. Call VimFuck function to interpret your brainfuck program.
3. You can ignore the initial errors on setup (known bug)
4. In case your brainfuck programs asks for input, type the input and call the macro

```
@c
```

5. Once done, you can call the macro

```
@z
```

to clean up.

## Demo
Here is a demonstration for User Input:
https://github.com/user-attachments/assets/67e953f5-85cb-4cbc-a47e-ba1e3dff6ec6


## Examples

Here's a simple "Hello, World!" example in Brainfuck:


```brainfuck
++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.
```

Here's a example to get 5 characters and print them:

```brainfuck
+++++[->,.<]
```

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve functionality, add new features, or fix bugs.

## License

This project is licensed under the MIT License.
