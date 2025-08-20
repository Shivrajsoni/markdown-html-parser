# Markdown to HTML Parser in Rust

A simple, lightweight library for converting Markdown to HTML, written in pure, safe Rust. This project aims to provide a straightforward and easy-to-use package for your Rust applications

## ✨ Features

Currently, the following Markdown syntax is supported:

- [x] Headings (`#`, `##`, `###`, etc.)
- [x] Bold text (`**text**`)
- [x] Italic text (`*text*`)
- [x] Links (`[display text](url)`)
- [x] Unordered Lists (`- list item`)

## 🏛️ Architecture

The conversion process happens in three main stages:

1.  **Lexing**: The input Markdown string is scanned and broken down into a sequence of "tokens". For example, `**hello**` becomes `[BoldStart, Text("hello"), BoldEnd]`.
2.  **Parsing**: The sequence of tokens is converted into a hierarchical structure called an Abstract Syntax Tree (AST). This tree represents the document's structure (e.g., a paragraph containing bold text).
3.  **Rendering**: The AST is traversed, and for each node in the tree, the corresponding HTML is generated.

## 🚀 Usage

1.  Add this library to your project's `Cargo.toml`:

    ```toml
    [dependencies]
    markdown-to-html-parser = "0.1.0"
    ```

2.  Use the `to_html` function in your code:

    ```rust
    // main.rs
    extern crate markdown_to_html_parser;

    fn main() {
        let markdown = "## Hello, World!\n\nThis is a **test** of our *new* parser.\n\n- Item 1\n- Item 2";
        let html = markdown_to_html_parser::to_html(markdown);
        println!("{}", html);
    }
    ```

## What's New in 0.1.0

*   Initial release of the `markdown-to-html-parser` crate!
*   Added support for basic Markdown features like headings, bold, italic, links, and unordered lists.

## Examples

Here are a few examples of the conversion in action.

**Input:**
````markdown
# Main Title

This is a paragraph with **bold** and *italic* text. Here is a [link to GitHub](https://github.com).

- First list item
- Second list item
````

**Output:**
```html
<h1>Main Title</h1>
<p>This is a paragraph with <strong>bold</strong> and <em>italic</em> text. Here is a <a href="https://github.com">link to GitHub</a>.</p>
<ul>
<li>First list item</li>
<li>Second list item</li>
</ul>
```

## 🤝 Contributing

This project is under active development. Contributions, issues, and feature requests are welcome!

```
