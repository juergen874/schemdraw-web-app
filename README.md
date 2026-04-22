# SchemDraw Web Runner

A simple web-based editor for [schemdraw](https://schemdraw.readthedocs.io/en/latest/), a Python library for producing high-quality electrical circuit schematic diagrams.

## Features

- **Live Python Editor**: Write `schemdraw` code directly in your browser.
- **Instant Rendering**: Generate SVG diagrams without installing Python locally.
- **Export to PDF**: Save your diagrams as high-quality PDF files.
- **Zero Backend**: Powered by [Pyodide](https://pyodide.org/), running Python entirely in the browser via WebAssembly.

## How to use

1. Wait for the environment to load (it will install `schemdraw` in the background).
2. Enter your Python code in the editor. Use the `d` object which is pre-initialized as a `schemdraw.Drawing()` instance.
3. Click **Render Diagram**.
4. Click **Export PDF** to print or save the diagram as a PDF.

## Example Code

```python
d += elm.Resistor().label('100Ω')
d += elm.Capacitor().down().label('10μF')
d += elm.Line().left()
d += elm.SourceV().up().label('12V')
```

## Hosting

This project is designed to be hosted on **GitHub Pages**.
https://juergen874.github.io/schemdraw-web-app/
## License

MIT
