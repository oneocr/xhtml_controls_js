<p align="center">
  <a href="https://oneocr.github.io/"><img src="https://oneocr.github.io/assets/mark.svg" width="76" height="76" alt="oneocr"></a>
</p>

<h1 align="center">oneocr-xhtml_controls_js</h1>

<p align="center">The viewer controls for the semantic XHTML output, written in Java and compiled to JavaScript by TeaVM.</p>

<p align="center">
  <a href="https://oneocr.github.io/">Website</a> ·
  <a href="https://github.com/oneocr">All repositories</a> ·
  <a href="https://oneocr.github.io/demo/sample-page.oneocr.xhtml">Live output</a>
</p>

---

## Overview

This Maven project produces `XHtmlOcrControls.js` - the interactive JavaScript that powers OCR document visualization features like:
- Background image toggle
- Line and word bounding boxes
- Confidence-based color coding  
- Layout mode switching
- Keyboard shortcuts (Ctrl+1-5)

## Architecture

- **Input**: Java source code with TeaVM annotations
- **Build Tool**: Maven with TeaVM plugin
- **Output**: `target/generated/js/XHtmlOcrControls.js`
- **Deployment Target**: GitHub Pages CDN at `https://oneocr.github.io/semantic_xhtml/`

## Build Requirements

- **JDK**: 11 or higher
- **Maven**: 3.6+
- **TeaVM**: Configured via Maven plugin
- **IDE**: NetBeans (recommended)

## Building

```bash
mvn clean compile
```

The generated JavaScript will be available at:
```
target/generated/js/XHtmlOcrControls.js
target/generated/js/XHtmlOcrControls.js.map
```

## Development Workflow

1. **Write Java Code**: Implement interactive features using TeaVM-compatible Java in NetBeans
2. **Build**: Run Maven to generate JavaScript
3. **Deploy**: Copy generated `XHtmlOcrControls.js` to the web repository for GitHub Pages hosting
4. **Test**: Verify functionality with XHTML OCR documents

## Pure Java Approach

This project maintains our commitment to pure Java development:
- **No Native Code**: FFM eliminated the need for C/C++ bindings
- **No Manual JavaScript**: TeaVM transpiles Java to browser-compatible JavaScript
- **No HTML Templating**: XHTML documents generated using Java DSL
- **Unified Skillset**: Pure Java team can contribute across the entire stack

## Why Java to JavaScript?

- **Type Safety**: Catch errors at compile time rather than runtime
- **IDE Support**: Full NetBeans support with code completion and refactoring
- **Team Consistency**: Pure Java team maintains productivity without context switching
- **Maintainability**: Structured OOP approach for complex interactive features

## Integration

The generated JavaScript is served via GitHub Pages CDN and dynamically loaded by OCR documents, ensuring:
- **Backward Compatibility**: Existing OCR documents continue to work
- **Independent Updates**: Controls can be upgraded without touching OCR documents
- **Clean Separation**: Document generation and presentation remain decoupled
- **Stable CDN URL**: Consistent access via GitHub Pages hosting

## Related Projects

- **Web Repository**: [semantic_xhtml](https://github.com/oneocr/semantic_xhtml) - GitHub Pages hosting for generated JavaScript
- **Document Generator**: [oneocr-cli](https://github.com/oneocr/cli) - Creates XHTML documents
- **Core API**: [oneocr-api](https://github.com/oneocr/api) - Java FFM bindings for Windows OCR

---

*Part of the OneOCR project (https://github.com/oneocr) - leveraging Windows 11 built-in OCR for Java applications.*