# Markdown Env

[Markdown](https://en.wikipedia.org/wiki/Markdown) is a lightweight markup language with plain text formatting syntax. It's designed so that it can be converted to HTML and many other formats using a tool by the same name.

This project will use some open source packages to build your own Markdown working environment. You can convert Markdown file to other formats in a easier way by using the tools provided in this project.

Note: Only support on Linux platform.

## Directories

- `bin/` - some shell scripts and dependent software
- `sample/` - recommended work env example

## Dependencies

- [wkhtmltox](https://wkhtmltopdf.org/): with patched qt. Converts an HTML page into a PNG format image and PDF format document.
- [markdown-styles](https://github.com/mixu/markdown-styles): Converts Markdown files to HTML, with over a dozen builtin themes. Default theme: github.
- `npm`: nodejs env

The packages `wkhtmltox` and `markdown-styles` have already been included in `bin/` directory. Note that `wkhtmltox` package is compiled in CentOS 7. Please visit https://wkhtmltopdf.org for more supports. The other dependencies like `npm` must be prepared by yourself. 

## Install

- Be sure all the dependencies mentioned above are ready on your platform.
- Copy `bin/` directory to your own executed directory and add it to the $PATH env variable. `~/bin` or `/usr/local/bin` is recommended.
- Recommend to create directory like `sample/` in your own Markdown working direcotry. See example to convert Markdown docs to HTML, PDF or PNG format files.

## Commands

- `md2html`: Convert Markdown file to HTML file. Default theme is `github`. See `markdown-styles` README for more information.
- `html2pdf`: Convert HTML file to PDF file
- `html2png`: Convert HTML file to PNG image file

## Example

```
[personal@your-env]$ cp README.md sample/markdown/
[personal@your-env]$ cd sample/
[personal@your-env]$ md2html --input markdown/README.md --output html/
[personal@your-env]$ html2pdf html/README.html pdf/README.pdf
[personal@your-env]$ html2png html/README.html images/README.png
```

