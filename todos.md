# Future Plans & Roadmap

This document outlines the future plans for this Markdown-to-HTML parser library. The primary goal is learning, with the ambition of creating a robust, production-ready Rust library that can eventually parse MDX and power a web-based conversion tool.

---

## 🎯 Short-Term Goals: Core Markdown Features

These are the next practical steps to build a complete and compliant Markdown parser.

- [ ] **Inline Code:** Support for `inline code snippets`.
- [ ] **Image Tags:** Implement the `![alt text](url)` syntax.
- [ ] **Blockquotes:** Support for `> quoted text`.
- [ ] **Ordered Lists:** Implement numbered lists, e.g., `1. First item`.
- [ ] **Fenced Code Blocks:** Support for multi-line code blocks using triple backticks (```), with optional language highlighting.
- [ ] **Horizontal Rules:** Implement rules using `---` or `***`.
- [ ] **Character Escaping:** Correctly handle escaped characters, like `\*` rendering as a literal asterisk.

---

## 🚀 Medium-Term Goals: Library Enrichment

These tasks focus on making the library robust, professional, and ready for use in production environments.

- [ ] **Comprehensive Error Handling:** Refactor the parser to return a `Result<Node, ParseError>` instead of panicking or failing silently on malformed Markdown. Provide clear error messages.
- [ ] **Performance Benchmarking:** Set up a benchmarking suite using `criterion.rs` to measure parsing speed and identify performance bottlenecks.
- [ ] **Refine Public API:**
    - [ ] Add configuration options (e.g., enabling/disabling certain features).
    - [ ] Consider exposing parts of the AST for advanced users.
- [ ] **Extensibility:** Design a plugin system (e.g., using traits) to allow users to add their own custom parsing rules.
- [ ] **Publish to Crates.io:** Prepare the package for a public release. This includes writing thorough documentation, choosing a license, and following best practices for publishing.

---

## 🌟 Long-Term Vision: MDX Support & Web Application

These are the ambitious goals that build on top of the solid library foundation.

- [ ] **MDX (Markdown + JSX) Support:**
    - [ ] **Lexer:** Teach the lexer to recognize JSX tags (`<Component />`) and `import`/`export` statements.
    - [ ] **AST:** Evolve the `Node` enum to represent JSX components, props, and import/export statements.
    - [ ] **Parser:** Implement the logic to parse the JSX syntax within the Markdown.
- [ ] **Web Application:**
    - [ ] **Compile to WebAssembly (WASM):** Compile the Rust parser to WASM so it can run efficiently in the browser.
    - [ ] **Frontend:** Build a user interface using a Rust frontend framework (like Yew or Leptos) that provides a text editor for input and a pane for the real-time rendered HTML output.
    - [ ] **Real-Time Conversion:** Use the WASM module to power instant MDX-to-HTML conversion directly in the user's browser.