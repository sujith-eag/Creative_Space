12/07/24

The struggle to make a editable PDF using Open office or Libre office draw, but when it was in an image format and not much could be done without OCR which mostly is paid or online, not suitable anything over 10pages.

Can i do this locally? is there some libraries that allows me to make it happen with few lines of code? i might not be putting up most of it, just stitching libraries but even that became challenging, trying to find non existent guides.
Even basic stuff, terminal installation, where to find the download, how to install, how to put it up or make it available for code, where is that file going, what the hell is the documentation saying and how and what to incorporate those into the code, how can i make it into a package when the dependencies are just in my pc, the errors after errors and kind of in the no guide zone was fun.

used few and researched few more things

OCRmyPDF
Ghostscript
Tesseract  pytesseract

PyMuPDF
pdfminer.six

leveraging each tool for its specific strengths: 
`ocrmypdf` for adding OCR text layers to PDFs, 
`Ghostscript` for preprocessing and converting PDFs to images (if needed), and 
`Tesseract` for OCR text extraction from those images. 

Yup this is my first interaction in ChatGPT also, and after so much looking around and being confused, the answers gave all the needed answers that had worked but took me around youtube, reddit, stackoverflow and soo many documentation sites but all was available so easily...

I didn't want to use it but if i have to fast pace this learning not on stumbling, then this has to be a way but moderated to get me out of blind spots and to explain me stuff.


import ocrmypdf

def ocr(file_path, save_path):
   ocrmypdf.ocr(file_path, save_path)
ocr("demo1.pdf","demoone.pdf")

[[Projects]]
