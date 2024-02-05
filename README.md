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
- `total time`: Total time to process all the files;
- `Conventional text`: How well the tool performs on conventional text
- `Multicolumn`: How well the tool performs on multicolumn pdf document
- `Table`: How well the tool process simple tables (each table line on 1 document) in pdf documents
- `Complex Table`: How well the tool process complex tables (some table lines are on multiple document lines)
- `Consistancy`: How well the tool is viable (performs the same good result on different documents)

Following, is the comparison table of the results

| library      | total time | Conventional Text | Multicolumn | Table | Complex table | consistancy |
| ------------ | ---------- | ----------------- | ----------- | ----- | ------------- | ----------- |
| pdfplumber   | 18s        | 3.5               | 1           | 2.5   | 2             | 2           |
| pdftotext    |            |                   |             |       |               |             |
| pymupdf      | 0.4s       | 4                 | 5           | 4     | 3             | 4           |
| pypdf2       | 7.8s       | 4.5               | 5           | 4     | 2.75          | 4           |
| unstructured | 17.7s      | 1                 | 4           | 1     | 2             | 1           |

