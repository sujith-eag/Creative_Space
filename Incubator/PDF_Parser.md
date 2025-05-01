
Inputs
* Provide a root directory containing the levels of sub directories which contain pdf files.
* A target folder to place the output of the program which will be text files or structure of folders with PDF
* Regex patterns to match to find the proper subject code, subject, semester, month year, exam type within the rendered text file to use for sorting, renaming the new files or old files and moving them to specific directories.

Program 
* Need to traverse through the main folder, to reach the end and find all the pdf present
* Convert them into text based files,
* parse the data to find the required text identifiers using regex
* Make the required folder in designated directory to place the file.
* Naming the folder as a combination of certain extracted key terms
* Moving the file to the dir, 
* Renaming the file according to set pattern using key terms.
* repeating for all files within each dirictory.

___
Issue with installing package, so creating a virtual envronment
```
sudo apt install python3-venv

# Moving to dir and setting up virtual env
python3 -m venv myenv

# activating
source myenv/bin/activate

# installation can happen here

decativate
```

```python
import pdfplumber
import os

def extract_pdf_text(pdf_path):
    """Extract text from a single PDF file."""
    with pdfplumber.open(pdf_path) as pdf:
        all_text = ""
        for page in pdf.pages:
            text = page.extract_text()
            if text:
                all_text += text
            else:
                print(f"Warning: No text found on page {page.page_number}")
        return all_text

def extract_text_from_folder(folder_path):
    """Process all PDFs in a folder and extract text."""
    extracted_texts = {}
    
    # List all files in the folder
    for filename in os.listdir(folder_path):
        if filename.endswith(".pdf"):  # Only process PDF files
            pdf_path = os.path.join(folder_path, filename)
            print(f"Extracting text from: {filename}")
            
            # Extract text from each PDF
            text = extract_pdf_text(pdf_path)
            extracted_texts[filename] = text
    
    return extracted_texts

# Usage example
folder_path = "path_to_your_folder"  # Replace with your folder path
extracted_data = extract_text_from_folder(folder_path)

# Print the extracted text for each PDF
for pdf_name, text in extracted_data.items():
    print(f"\nText from {pdf_name}:")
    print(text[:500])  # Print first 500 characters of each PDF's text for brevity


```

```python
def extract_text_from_folder_recursive(folder_path):
    """Process all PDFs in a folder and subfolders recursively."""
    extracted_texts = {}
    
    # Walk through all files in folder and subfolders
    for dirpath, dirnames, filenames in os.walk(folder_path):
        for filename in filenames:
            if filename.endswith(".pdf"):  # Only process PDF files
                pdf_path = os.path.join(dirpath, filename)
                print(f"Extracting text from: {filename}")
                
                # Extract text from each PDF
                text = extract_pdf_text(pdf_path)
                extracted_texts[filename] = text
    
    return extracted_texts

```

```python
import pdfplumber

def extract_pdf_tables(pdf_path):
    with pdfplumber.open(pdf_path) as pdf:
        tables = []
        
        # Iterate through each page in the PDF
        for page in pdf.pages:
            # Extract tables from the page
            page_tables = page.extract_tables()
            
            # If tables are found, add them to the list
            if page_tables:
                tables.extend(page_tables)
        
        return tables

# Usage example
pdf_path = "your_pdf_with_tables.pdf"
extracted_tables = extract_pdf_tables(pdf_path)

# Print the tables
for table in extracted_tables:
    for row in table:
        print(row)

```
____

Linux 


### 1. **Command-line Tools (Linux-based)**

#### a. **pdftotext** (from the `poppler-utils` package)

- **Description**: One of the most common tools for extracting text from PDFs in Linux. It's very efficient and works well for most PDF files.
- **How to Use**:

```
pdftotext input.pdf output.txt
```

If you want the output directly in the terminal:

```
pdftotext input.pdf -
```

- **Pros**:
- Fast and simple to use.
- Handles a variety of PDFs well.
- Can be used as part of shell scripts.
- **Cons**:
- Might struggle with heavily formatted or scanned PDFs (though it supports OCR if the right libraries are available).

#### b. **pdftohtml** (also part of `poppler-utils`)

- **Description**: Converts PDFs to HTML format, which may be easier to parse than raw text, especially for complex PDFs.
- **How to Use**:

```
pdftohtml input.pdf output.html
```

- **Pros**:
- Good for extracting structured content.
- HTML output makes it easier to preserve formatting.
- **Cons**:
- May not work well with scanned PDFs.

#### c. **OCR with Tesseract**

- **Description**: If the PDF is a scanned image (not a text-based PDF), `Tesseract` OCR can be used to extract text.
- **How to Use**: Convert the PDF to images first (e.g., using `pdftoppm`), then apply OCR:

```
pdftoppm input.pdf output -png
tesseract output-1.png output.txt
```

- **Pros**:
- Can extract text from scanned images.
- **Cons**:
- Less accurate than text extraction methods.
- Slower.
