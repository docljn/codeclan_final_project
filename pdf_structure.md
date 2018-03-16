# Understanding pdf files

## Overview of pdf file structure

### A pdf file is organised into four parts:
- a one-line header
  - specifies the pdf specification version
  - always starts with %
- a body
  - contains the document's contents in the form of objects
  - visible objects:
    - text streams
    - image data
    - fonts
    - annotations
  - invisible objects:
    - implement interactivity, security features, logical structure
- a cross-reference table
  - offsets to all the objects in the file
  - means any object can be found directly without scanning large portions of the file
- a trailer (aka trailer dictionary)
  - file size
  - object reference to catalogue object (pointers to document object trees)
  - info dictionary
- there is also an end of file marker & information
  - applications read pdf files from the end
  - the lines immediately below the trailer and above the %%EOF marker provide the offset to the cross-reference table

A .pdf file is never over-written, merely added to...

**References**

Adobe PDF reference centre:
https://www.adobe.com/devnet/pdf.html

http://www.mactech.com/articles/mactech/Vol.15/15.09/PDFIntro/index.html
https://stackoverflow.com/questions/6562235/how-to-open-pdf-raw#6562443

Tools for inspecting pdf structure:
- QPDF may be worth a look  
http://qpdf.sourceforge.net
https://github.com/qpdf/qpdf
- Linux only PDFEdit
http://pdfedit.cz/en/index.html
- Windows only PDFCosEdit
http://www.pdftron.com/pdfcosedit/index.html
