 Overview
This project implements an Apple Detection API using FastAPI and classical computer vision techniques. The system processes uploaded images, detects apples based on color segmentation and contour analysis, and returns the number of apples detected.

This serves as a lightweight, efficient alternative to deep learning-based object detection, making it ideal for real-time applications and low-power edge devices.

🚀 Features
✅ FastAPI REST API for image-based apple detection
✅ Color-based segmentation (HSV) for red apple detection
✅ Contour detection & bounding boxes using OpenCV
✅ Handles real image uploads with proper error handling
✅ Modular & scalable architecture for future multi-fruit detection

🛠️ Technologies Used
FastAPI → Lightweight & high-performance web framework for the API
OpenCV → Classical image processing for object detection
NumPy → Efficient image manipulation
Uvicorn → ASGI server for FastAPI
Jupyter Notebook → Development environment
📡 API Endpoints
Method	Endpoint	Description
POST	/detect_fruits	Upload an image and detect apples
GET	/docs	Interactive API documentation
📌 Example Request (/detect_fruits)
bash
Copy
Edit
curl -X 'POST' 'http://127.0.0.1:8000/detect_fruits' \
  -H 'accept: application/json' \
  -H 'Content-Type: multipart/form-data' \
  -F 'file=@apple_test.jpg'
📌 Example JSON Response
json
Copy
Edit
{
  "color": {"apple": 2}
}
🔄 Future Enhancements
🔹 Multi-fruit detection (Bananas, Oranges, etc.)
🔹 Template matching for more robust detection
🔹 Edge AI deployment on Raspberry Pi / Jetson Nano
🔹 Integration with deep learning models (YOLO, MobileNet, etc.)

📌 How to Run Locally
bash
Copy
Edit
# Clone the repository
git clone https://github.com/your-username/apple-detection-api.git
cd apple-detection-api

# Install dependencies
pip install -r requirements.txt

# Run the API
uvicorn main:app --reload

# Open API docs
http://127.0.0.1:8000/docs

Guneet Singh 
https://www.linkedin.com/in/guneet-singh-16a5b5225/
guneetsingh792@gmail.com
