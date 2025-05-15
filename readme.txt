# Adverse Conditions License Plate Detection

This project provides a robust deep learning-based pipeline for automatic license plate detection and recognition in challenging weather conditions, including fog, rain, snow, low light, and intense sunlight. By combining weather classification, adaptive denoising, object detection, and OCR, the system improves license plate visibility and recognition accuracy in real-world environments.

## 🚗 Key Features

- Weather classification using ResNet-18
- Condition-specific denoising techniques
- YOLO-based license plate detection
- OCR-based character recognition (PaddleOCR)
- End-to-end pipeline for real-time or video-based processing

---

## 🧠 Methodology

1. **Weather Classification**  
   A ResNet-18 CNN is trained on labeled video frames (sunny, rainy, foggy, lowlight, snowy) to predict the dominant weather condition.

2. **Condition-Specific Denoising**  
   Based on the predicted condition, a tailored image enhancement method is applied:
   - Foggy → Dark Channel Prior
   - Rainy → Rain streak removal
   - Lowlight → Histogram equalization/Gamma correction
   - Snowy → Contrast and blur balancing
   - Sunny → Glare/saturation correction

3. **License Plate Detection**  
   YOLO (You Only Look Once) is used to detect license plates from enhanced frames.

4. **Text Recognition**  
   PaddleOCR extracts readable license plate text from detected regions.


