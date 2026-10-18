# ConvertX

**A simple, portable command-line file converter for Windows.**

[⬇️ Download ConvertX Portable](https://github.com/amitpadhyart/ConvertX/releases/latest/download/ConvertX-Portable.zip)

ConvertX is a side project built to make file conversion simple from the command line. The goal is to provide a convenient tool for converting documents, spreadsheets, and images without having to open multiple applications manually.

> **This is a side project!** If you find it useful or want to see it grow, please ⭐ star this repository on GitHub. If there's interest, I'll continue working on ConvertX, fixing bugs, adding formats, and making it better.

## ✨ Features

ConvertX supports a range of file conversions, including:

- **PDF:** Convert PDF files to TXT, DOC, DOCX, and images.
- **Word documents:** Convert DOCX files to TXT and PDF.
- **Spreadsheets:** Convert XLSX files to CSV and PDF, and CSV files to XLSX.
- **Text files:** Convert TXT files to PDF and DOCX.
- **Images:** Convert supported images to PDF and other image formats.
- **OCR tools:** Includes bundled Tesseract components for future and supported OCR workflows.

*Conversion availability and output quality depend on the input format and the conversion method. PDF-to-DOCX conversion may not preserve the original layout, images, or tables perfectly.*

## 🚀 Getting Started

### 1. Download

Download the latest portable package from the [ConvertX Releases page](https://github.com/amitpadhyart/ConvertX/releases/latest).

### 2. Extract

Extract `ConvertX-Portable.zip` to a folder, for example:

`C:\ConvertX`

The portable package is designed to include its Java runtime and conversion tools, so you don't need to install Java, Maven, LibreOffice, or Tesseract separately.

### 3. Open Command Prompt

Navigate to the extracted folder:

```bat
cd /d C:\ConvertX
```

### 4. Check the application

Run:

```bat
convertx.cmd --version
```

To see the available commands:

```bat
convertx.cmd --help
```

You can also launch `ConvertX.exe` directly.

## 💻 Usage

The basic command structure is:

```bat
convertx.cmd convert "input-file" to .extension -o "output-file"
```

### Examples

**Convert PDF to text**

```bat
convertx.cmd convert "report.pdf" to .txt -o "report.txt"
```

**Convert PDF to DOCX**

```bat
convertx.cmd convert "report.pdf" to .docx -o "report.docx"
```

**Convert DOCX to PDF**

```bat
convertx.cmd convert "document.docx" to .pdf -o "document.pdf"
```

**Convert an image to PDF**

```bat
convertx.cmd convert "photo.png" to .pdf -o "photo.pdf"
```

**Convert XLSX to CSV**

```bat
convertx.cmd convert "data.xlsx" to .csv -o "data.csv"
```

Replace the example filenames with the paths to your own files. If a path contains spaces, put it inside quotation marks.

## 🛠️ Technology Stack

- **Java** — application and conversion logic
- **Spring Boot** — local conversion API
- **Apache PDFBox** — PDF processing
- **Apache POI** — Word and Excel document processing
- **LibreOffice** — document conversion
- **Tesseract OCR** — OCR tooling

## 📦 Portable Package

The portable distribution is intended to run directly after extraction. It contains the application launcher, private Java runtime, CLI scripts, and bundled conversion tools.

No traditional installer is required. Extract the ZIP and run the application.

## 🧑‍💻 For Developers

Want to explore or contribute to ConvertX?

1. Star the repository ⭐.
2. Clone the repository.
3. Install a compatible JDK and Maven.
4. Obtain the required third-party conversion tools.
5. Build the project.

```bash
git clone https://github.com/amitpadhyart/ConvertX.git
cd ConvertX
mvn clean package
```

The portable distribution and developer build have different requirements. The source repository does not include the bundled third-party tools, so follow the project instructions to obtain them before testing conversions that depend on those tools.

## 🗺️ Roadmap

Possible future improvements include:

- Better PDF-to-Word layout preservation
- More conversion formats
- Improved error messages and validation
- Better OCR integration
- Faster processing for large files
- Easier installation and distribution
- Automated tests and improved documentation

## 🤝 Support the Project

ConvertX started as a side project, and there's plenty of room to improve it.

If you like the idea, please **star the repository** ⭐. If people are interested, I'll keep working on it and make it better.

Bug reports, feature suggestions, and contributions are welcome!

## 📄 License

Check the repository for licensing information before redistributing or modifying ConvertX.
