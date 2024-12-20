# Smart Image Processor

**A Python-powered image processing tool that enhances images, detects objects, recognizes faces, extracts text, and applies custom filters.**

## Features

1. **Image Enhancement**
   - Automatic brightness, contrast, and color adjustments.
   - Noise reduction and sharpening filters.

2. **Object Detection**
   - Detect objects in images using pre-trained YOLO models.
   - Draw bounding boxes around detected objects with labels.

3. **Facial Recognition**
   - Identify and highlight faces in images.
   - Optional: Blur or replace faces for privacy concerns.

4. **OCR (Optical Character Recognition)**
   - Extract text from images using Tesseract OCR.
   - Export extracted text to a file.

5. **Custom Filters**
   - Apply artistic filters like grayscale, sepia, and cartoon effects.

6. **Batch Processing**
   - Resize and format multiple images in one go.

7. **Optional REST API**
   - Upload and process images via an API built with Flask.

---

## Tech Stack

- **Programming Language**: Python
- **Libraries**:
  - OpenCV: For image processing and analysis.
  - Pillow: For image enhancement and manipulation.
  - pytesseract: For OCR functionality.
  - Flask: For optional API integration.
  - PyTorch/TensorFlow: For AI-driven object detection (optional).

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ImageProcessor.git
   cd ImageProcessor
   ```

2. Set up a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. Install the required dependencies:
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
2. Use a tool like Postman to send requests to the API endpoint:
   ```
   POST http://127.0.0.1:5000/process-image
   Body: Form-data (key: 'file', value: [your image file])
   ```

---

## Example Outputs

| Feature           | Example Output |
|-------------------|----------------|
| **Enhanced Image**| ![enhanced_image](examples/enhanced_image.jpg) |
| **Object Detection** | ![detected_objects](examples/detected_objects.jpg) |
| **Facial Recognition** | ![faces_detected](examples/faces_detected.jpg) |
| **Text Extraction** | Extracted text saved to `extracted_text.txt`. |

---

## Future Enhancements

- Add cloud deployment for scalability.
- Integrate advanced AI features like segmentation and pose estimation.
- Include a user-friendly GUI using Tkinter or PyQt.

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
- **Pillow** for image manipulation.
- **Tesseract** for OCR capabilities.
- **YOLO** for object detection models.
