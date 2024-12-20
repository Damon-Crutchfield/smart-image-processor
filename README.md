# Smart Image Processor

**A Python-powered tool to enhance images, detect objects, recognize faces, extract text, and apply custom filters. Built for both personal and professional use, with optional REST API integration.**

## Features

1. **Image Enhancement**
   - Automatically adjust brightness, contrast, and sharpness.
   - Apply artistic filters like grayscale and sepia.

2. **Object Detection**
   - Detect objects using pre-trained YOLO models.
   - Draw bounding boxes and label detected objects.

3. **Facial Recognition**
   - Highlight faces in images.
   - Optional: Blur or mask faces for privacy.

4. **OCR (Optical Character Recognition)**
   - Extract text from images using Tesseract OCR.
   - Export text to a `.txt` file.

5. **Batch Processing**
   - Resize and reformat multiple images simultaneously.

6. **Optional REST API**
   - Upload and process images via an API built with Flask.

---

## Tech Stack

- **Programming Language**: Python
- **Core Libraries**:
  - OpenCV: For image processing and object detection.
  - Pillow: For image enhancement and manipulation.
  - pytesseract: For OCR functionality.
  - Flask: For REST API integration.
  - YOLO: For object detection models.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/smart-image-processor.git
   cd smart-image-processor
   ```

2. Set up a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Install Tesseract OCR:
   - **Ubuntu**:
     ```bash
     sudo apt update
     sudo apt install tesseract-ocr
     ```
   - **Mac**:
     ```bash
     brew install tesseract
     ```
   - **Windows**:
     [Download and install Tesseract](https://github.com/UB-Mannheim/tesseract/wiki).

---

## Usage

### Local Script

1. Place your test image in the project folder.
2. Run the script:
   ```bash
   python main.py
   ```
3. Follow the prompts to apply desired features.

### REST API (Optional)

1. Start the server:
   ```bash
   flask run
   ```
2. Use a tool like Postman to send a request to the API endpoint:
   ```
   POST http://127.0.0.1:5000/process-image
   Body: Form-data (key: 'file', value: [your image file])
   ```

---

## Example Outputs

| Feature           | Example Output |
|-------------------|----------------|
| **Enhanced Image**| ![Enhanced Image](examples/enhanced_image.jpg) |
| **Object Detection** | ![Object Detection](examples/detected_objects.jpg) |
| **Facial Recognition** | ![Facial Recognition](examples/faces_detected.jpg) |
| **Text Extraction** | Extracted text saved to `extracted_text.txt`. |

---

## Future Enhancements

- Add advanced AI features like segmentation and pose estimation.
- Include a user-friendly GUI using Tkinter or PyQt.
- Deploy the API to cloud platforms for broader accessibility.

---

## Contributing

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature description"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- **OpenCV** for image processing.
- **Pillow** for image enhancement.
- **Tesseract OCR** for text extraction.
- **YOLO** for object detection models.
