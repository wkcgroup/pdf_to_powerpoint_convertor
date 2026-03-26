# 📄 PDF to PowerPoint Converter (Colab Notebook)

**Overview**

This notebook provides a simple, automated workflow to convert a PDF document into a PowerPoint presentation (.pptx).

Each page of the PDF is converted into a corresponding slide using one of two approaches:

Image mode → each page becomes a high-resolution image on a slide
Text mode → text is extracted and formatted into slides (where possible)

The workflow is designed for quick use in Google Colab, requiring minimal setup.


**🚀 Features**

Convert entire PDFs into PowerPoint slides in seconds
Supports:

🖼️ Image-based conversion (high fidelity, preserves layout)

📝 Text-based conversion (editable content)

Adjustable DPI for image quality

Automatic slide sizing based on PDF page dimensions

Built-in upload/download interface (Colab-friendly)

Session clean-up utility

**🧰 Dependencies**

The notebook installs required libraries automatically:

pymupdf (fitz)

python-pptx

**📂 Workflow 1. Install Libraries**

The notebook installs required packages at runtime:

!pip install -q pymupdf python-pptx

2. Upload PDF

You will be prompted to upload a PDF file:

from google.colab import files

uploaded = files.upload()

3. Configure Conversion Settings

**Key parameters:**

mode = "image"   # "image" or "text"

dpi = 220        # used in image mode only

Modes explained:

Mode	Description

image	Converts each page into an image (best for layouts, maps, reports)

text	Extracts text into slides (best for simple documents)

**4. Convert PDF → PowerPoint**

**The notebook:**

Reads each PDF page using PyMuPDF

Creates a PowerPoint using python-pptx

Matches slide size to PDF dimensions

Inserts content based on selected mode

**5. Download Output**

files.download("converted.pptx")

**6. Clean Up (Optional)**

Removes temporary files from the session:

**Deletes all PDFs and PPTX files**
