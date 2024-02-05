# Benchmark of some PDF-to-text python libraries
The aim of this repo is to compare some tools to process pdf into text.
The tools are :
- [pdfplumber](https://github.com/jsvine/pdfplumber) : made by [jsvine](https://github.com/jsvine) for detailed information about each char, rectangle, line, et cetera — and easily extract text and tables.
- [pdftotext](https://pypi.org/project/pdftotext/) : A simple PDF text extraction.
- [pymupdf](https://pymupdf.readthedocs.io/en/latest/): a high-performance Python library for data extraction, analysis, conversion & manipulation of PDF (and other) documents.
- [pypdf2](https://pypi.org/project/PyPDF2/): A pure-python PDF library capable of splitting, merging, cropping, and transforming PDF files.
- [unstructured](https://github.com/Unstructured-IO/unstructured): an Open source libraries and APIs to build custom preprocessing pipelines for labeling, training, or production machine learning pipelines.

## Comparison
To compare the libraries, we used 3 PDF files:
- `multicolunm-code-travail-cmr.pdf`: A multicolumn file containing the Cameroonian Labor Code
- `wtables-benin-LF-2023.pdf`: A conventional PDF with some tables
- `wtables-food-calories.pdf`: Another conventional PDF with some tables

For each library we extract the text from all files. Then give an annotation on a scale of 1 to 5 for each comparison criteria.
Following, is the comparison table of the results

| library      | Conventional Text | Handle Multicolumn | Handle Table |
| ------------ | ----------------- | ------------------ | ------------ |
| pdfplumber   |                   |                    |              |
| pdftotext    |                   |                    |              |
| pymupdf      |                   |                    |              |
| pypdf2       |                   |                    |              |
| unstructured |                   |                    |              |

