---
layout: default
title: Python setup MacOS
---
### Install miniconda: download .pkg from miniconda website and install
### Check installation and python version using terminal
`which python`
`python --version`
### Update conda using terminal
`conda update conda`
### Conda cheat sheet: common conda commands
> [https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html](URL)
### Create new virtual environment named  *'testenv'*  with bare python essentials
`conda create --name testenv python`
### Switch to the 'testenv' environment
`conda activate testenv`
### Install required packages in the testenv
`conda install jupyterlab`
### Start Jupyter lab in the current environment
`jupyter lab`
### Markdown commands in jupyter lab
- Headings: ` # , ##, ###, #### `
- Make text ITALIC: ` *Italic* `
- Make text BOLD: ` **Bold** `
- List item as a bullet: dash and space ` -  `
- List item as a number: Simple as number and dot ` 1. ` <br>(keep using 1. for every line. It will automatically number in order)
- Indenting text: Greater than and space ` > `
- Inline code span: Back quotation mark ` ` `
- Block of code: Triple back quotation marks ` ``` `
- Mathematical symbol: `$ symbols $`
- Horizontal lne: On a new line, enter three asterix ` *** `
- Link a section: `[Title of Section](#title-of-section)`
- Hyperlink: `[Text](URL)`


