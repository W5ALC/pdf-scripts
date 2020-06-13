# PDF Scripts

Scripts (mostly Bash) to repair, verify, OCR, compress (etc.) PDFs.

## Overview

### [repair_pdf.sh](./repair_pdf.sh)

Using: `pdftocairo` from [poppler](<https://en.wikipedia.org/wiki/Poppler_(software)>), `mutool clean` from [MuPDF](https://en.wikipedia.org/wiki/MuPDF), [qpdf](https://en.wikipedia.org/wiki/QPDF)

Caveat: May remove text in OCRd PDFs. Use `--check` to avoid conversion to preserce text in OCRd PDFs.

Related Work: https://github.com/NicolasBernaerts/ubuntu-scripts/blob/master/pdf/pdf-repair

### [verify_pdf.sh](./verify_pdf.sh)

Checks if text can be extracted (if it's already on the PDF)

### [compress_pdf.sh](./compress_pdf.sh)

Using [ghostcript](https://askubuntu.com/a/256449) to compress images in PDFs.

### [reduce_size_pdf.sh](reduce_size_pdf.sh)

Use [compress_pdf.sh](./compress_pdf.sh) but also [pdfsizeopt](https://github.com/pts/pdfsizeopt) to reduze file size of PDFs.

### [ocr_pdf.sh](./ocr_pdf.sh)

OCR PDFs with [OCRmyPDF](https://github.com/jbarlow83/OCRmyPDF).

### [clean_metadata_pdf.sh](./clean_metadata_pdf.sh)

Remove metadata with [exiftool](https://exiftool.org/).

### [is_ocrd_pdf.sh](./is_ocrd_pdf.sh)

Detect OCRd PDFs. See also [sort_ocrd_pdfs.sh](sort_ocrd_pdfs.sh) to sort PDFs.

### [pipeline.sh](./pipeline.sh)

Combining several of the above scripts.

## Development

- focus on Bash v4+
- write Python 3.6+ scripts if Bash gets too complicated
- use Docker images if available
- should run on the major Unix-like OSs (Linux (e.g. Ubuntu), macOS)
- format code with [shfmt](https://github.com/mvdan/sh#shfmt), e.g., extension for [VS Code](https://github.com/foxundermoon/vs-shell-format)
- lint scripts with [shellcheck](https://github.com/koalaman/shellcheck), e.g., extension for [VS Code](https://github.com/timonwong/vscode-shellcheck)

## License

GPLv3.
