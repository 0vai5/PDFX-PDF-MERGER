 ## PDFX-merger 

### Introduction

PDFX-merger is a simple Node.js application that allows users to merge multiple PDF files into a single PDF file. The application uses the [pdf-merger-js](https://www.npmjs.com/package/pdf-merger-js) library to merge the PDF files.

### Installation

To install PDFX-merger, clone the repository and install the dependencies:

```
git clone https://github.com/your-username/pdfx-merger.git
cd pdfx-merger
npm install
```

### Usage

To use PDFX-merger, first start the server:

```
npm start
```

Then, open your browser and go to http://localhost:3000. You will see a form that allows you to select two PDF files to merge. Select the files and click the "Merge" button. The merged PDF file will be downloaded to your computer.

### Code Explanation

The following is a step-by-step explanation of the code in PDFX-merger:

1. The `merge.js` file imports the `PDFMerger` class from the `pdf-merger-js` library. It also creates a new instance of the `PDFMerger` class.
2. The `merge` function takes two parameters, `p1` and `p2`, which are the paths to the two PDF files to be merged. The function first adds the first PDF file to the `PDFMerger` instance. Then, it adds the second PDF file to the `PDFMerger` instance, but only the second page of the file.
3. The `merge` function then saves the merged PDF file to the `public` directory. The file is given a unique name based on the current time.
4. The `server.js` file imports the `express` and `multer` libraries. It also creates a new instance of the `express` application.
5. The `server.js` file uses the `express.static` middleware to serve the static files in the `public` directory.
6. The `server.js` file defines a route for the `/merge` endpoint. This endpoint uses the `multer` middleware to parse the multipart/form-data request body. The `merge` function is then called to merge the two PDF files.
7. The `server.js` file starts the `express` application

