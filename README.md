# 🖐️ HandDraw AI – Gesture-Based Math Solver

Draw with your hands, capture equations, and let AI solve them for you. This project uses Computer Vision to detect hand gestures for drawing and Google Gemini to interpret and solve handwritten math problems.

## 🚀 Features
- ✍️ Draw using your index finger with hand tracking.
- 🎨 Select brush colors and eraser with gestures.
- 📸 Automatically capture when thumb + index are raised.
- 🧠 Solve handwritten math with Gemini AI.
- 🌐 Live video feed in a web interface.
- 

### ✅ Use Cases
| Use Case | Description |
|----------|-------------|
| ✍️ **Gesture-Based Whiteboard** | Draw using hand gestures for education, brainstorming, or remote collaboration. |
| 🧮 **Math Solver** | Handwrite an equation on the screen and let AI solve it visually. |
| 🎓 **AI Tutor Interface** | Can evolve into a gesture-controlled tutoring tool with voice + response. |
| 🖥️ **Touchless Interfaces** | Useful for public kiosks, AR displays, or accessibility-focused UIs. |

---

### 🔍 Models Used

| Layer | Model | Type | Description |
|-------|-------|------|-------------|
| **Hand Detection** | MediaPipe Hands | CNN | Real-time hand detection & 3D landmark tracking (21 keypoints) |
| **Gesture Logic** | Custom Rules | Logic-based | Detects drawing/selecting/triggering via hand landmark geometry |
| **Math Solver** | Gemini 1.5 Pro | Multimodal LLM | Reads handwritten math problems and returns solution with explanation |
| **Canvas Preprocessing** | OpenCV Filters | Image Ops | Thresholding, bitwise ops, and blending for clear canvas output |

---

### 🏗️ Full Tech Stack

| Layer | Technology | Purpose |
|-------|------------|---------|
| 🧠 **AI/ML** | Google Gemini Pro | Solves handwritten math via image + prompt |
| 👁️ **CV & Tracking** | MediaPipe, OpenCV | Hand landmark detection, gesture control, drawing logic |
| 🖼️ **Image Processing** | NumPy, OpenCV | Canvas rendering, image capture, thresholding |
| 🌐 **Web Backend** | Flask | Live video streaming, Gemini API integration |
| 🔐 **Env Management** | python-dotenv | Securely manage API keys |
| 📁 **Assets/UI** | Header images | Custom UI brush selection |
| 🌍 **Frontend** | HTML (via Flask Jinja2) | Render canvas and Gemini output |
"""



## 📷 Screenshots

<img width="1920" height="1080" alt="Screenshot 2025-07-29 213736" src="https://github.com/user-attachments/assets/2d3c521f-8b2e-4998-a36f-8c415e11a3f5" />
<img width="1920" height="1080" alt="Screenshot 2025-07-29 213630" src="https://github.com/user-attachments/assets/0cf0955d-778b-4cff-9428-2663ed2d2616" />
<img width="1920" height="1080" alt="Screenshot 2025-07-29 213042" src="https://github.com/user-attachments/assets/ba7f1033-1f32-45d3-a00c-90660fbd96fb" />
<img width="1920" height="1080" alt="Screenshot 2025-07-29 213023" src="https://github.com/user-attachments/assets/32fe55e5-b4e6-4dda-94b4-e1d745392fb6" />

## 💡 Future Scope

- ✍️ **Handwriting OCR Preprocessing**: Add adaptive thresholding or contour detection to clean the canvas before sending to Gemini.
- 📊 **Math OCR Integration**: Use tools like MathPix or Tesseract for equation validation before sending to LLM.
- 🧠 **Custom Gesture Classifier**: Add more gestures for undo, clear, or save.
- 🔡 **Voice Output**: Use TTS (like pyttsx3 or gTTS) to read out the Gemini solution.
- ☁️ **Cloud Hosting**: Deploy the app using Docker + AWS/GCP + NGINX for real-time usage.

