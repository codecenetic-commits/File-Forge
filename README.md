# FileForge

FileForge is a lightweight, browser-based file conversion tool built as a single static HTML page. It supports client-side conversion of documents and images without uploading files to a server, so your files remain private and secure.

## Features

- Drag & drop file upload
- Multiple file support
- Convert between common document and image formats
- Client-side processing using browser APIs
- Automatic format detection
- Conversion progress and result download
- Download all converted files as a ZIP archive
- Conversion history stored locally in browser storage
- Light / dark theme toggle
- Responsive layout for desktop and mobile

## Supported Input Formats

- PDF (`.pdf`)
- DOCX (`.docx`)
- TXT (`.txt`)
- JPG / JPEG (`.jpg`, `.jpeg`)
- PNG (`.png`)
- WebP (`.webp`)

## Supported Output Formats

- PDF
- DOCX
- TXT
- JPG
- PNG
- WebP

## Supported Conversion Paths

- Image → Image (`jpg`, `png`, `webp`)
- Image → PDF
- TXT → PDF
- TXT → DOCX
- DOCX → TXT
- PDF → TXT

> Note: Some complex conversions such as `PDF → DOCX`, `DOCX → PDF`, and same-format conversions are handled as best-effort client-side conversions with a textual placeholder notice rather than full fidelity reconstruction.

## Getting Started

### Option 1: Open directly in a browser

1. Open `html.html` in your browser.
2. Drag and drop files into the upload area or click to browse.
3. Choose the output format.
4. Click **Convert Now**.
5. Download individual results or use **Download All as ZIP**.

### Option 2: Serve locally with a web server

If you prefer to run the file via a local web server, use any static file server. For example, with Python:

```bash
cd "e:/Bilal Projects/Tools/File Formet convertor"
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/html.html
```

## Dependencies

FileForge uses the following browser-side libraries from CDNs:

- `pdf-lib` for PDF creation and manipulation
- `mammoth.js` for extracting text from DOCX files
- `FileSaver.js` for downloading converted results
- `JSZip` for creating ZIP archives
- `pdf.js` for extracting text from PDF pages
- `Font Awesome` for UI icons

## Browser Compatibility

This tool is designed for modern browsers with support for:

- `File` / `FileReader`
- `Blob`
- `Canvas`
- `fetch` / `Promise`
- `localStorage`

## Project Structure

- `html.html` — main application page containing markup, styles, and conversion logic
- `README.md` — project documentation

## Usage Tips

- Keep uploaded files under 100MB each
- Use the recommended output format for best results
- When converting from PDF or DOCX to other formats, text extraction is performed in-browser and may not preserve advanced formatting
- Image conversions use the browser canvas and may alter image quality slightly depending on the format

## License

This project is provided as-is. Feel free to use or adapt it for your own tools and workflows.
