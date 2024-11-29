# Contert-PNG-JPG-to-Webp

This project provides a client-side tool for converting PNG and JPG images inside a ZIP archive into WEBP format. Along with the conversion, it allows users to add metadata like titles, author names, and descriptive phrases to the output files. 

## Features

- Converts images in a ZIP archive (PNG, JPG, JPEG) to WEBP format.
- Adds metadata (e.g., image titles, photographer name, and SEO-friendly keywords) to the file names.
- Works entirely on the client-side; no data is sent to a server.
- Provides a user-friendly interface with progress updates.
- Automatically generates descriptive and unique file names.

## How It Works

1. **Upload a ZIP file** containing PNG or JPG images.
2. **Fill out the input fields**:
   - **Store Title**: Adds a descriptive title to each image.
   - **Photo Author**: Includes the photographer's name in the metadata.
   - **Phrases**: Adds SEO-friendly keywords to the file names.
3. **Click Submit**: The tool processes the ZIP file, converts the images to WEBP, and adds metadata.
4. **Download the Result**: A new ZIP file containing the converted images is generated for download.

## File Name Format

The output images will follow this naming convention:  
`<first_image_name>_<phrases>_<storeTitle>-AutoreFoto:<photoAuthor>_<uniqueId>.webp`

For example:  
`image1_nature_sunset_MyStore-AutoreFoto:JohnDoe_1675648392347.webp`

## Installation

No installation required. Open the provided HTML file in a browser and start using the tool.

## Usage

1. Open the web page in a browser.
2. Upload a ZIP file containing your images.
3. Fill in the metadata fields:
   - **Store Title**
   - **Photographer Name**
   - **Keywords** (comma-separated phrases for SEO)
4. Submit the form and wait for the conversion to complete.
5. Download the processed ZIP file.

## Code Overview

### Main Functions

1. **`processFiles(zipFile, storeTitle, photoAuthor, phrases)`**
   - Handles the processing of files: extraction, conversion, metadata addition, and ZIP creation.

2. **`convertImagesInZip(zipFile, storeTitle, photoAuthor, phrases)`**
   - Reads the ZIP file, converts images to WEBP format, and appends metadata to filenames.

3. **`convertToWebP(blob)`**
   - Converts a single image file to WEBP format using a `<canvas>` element.

4. **`createZipFromFiles(files)`**
   - Creates a new ZIP file containing the converted images.

5. **`updateProgressBar(value)`**
   - Updates the progress bar as images are processed.

6. **`downloadBlob(blob, filename)`**
   - Triggers the download of the final ZIP file.

### Dependencies

This project uses the [zip.js](https://gildas-lormeau.github.io/zip.js/) library for ZIP file manipulation.

## Error Handling

- Displays an alert if any required field is missing.
- Logs errors during file processing in the browser console.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss potential changes or improvements.

## Acknowledgments

- [zip.js Library](https://gildas-lormeau.github.io/zip.js/) for ZIP file handling.
- Inspired by the need for a client-side, privacy-friendly image conversion tool.
