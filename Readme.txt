Computer Vision Music Player 🎵✋
Project Description
A hand-tracking application that plays different musical notes (WAV files) when specific fingers are lowered. Uses computer vision to detect finger positions and triggers corresponding sound effects in real-time.

Features
Real-time hand tracking with MediaPipe

Finger position detection

Sound playback with Pygame

Multi-hand support (up to 2 hands)

Visual feedback of hand landmarks

📁 File Structure
ComputerVisionMusic/
├── main.py            # Main application code
├── A.wav              # Musical note samples
├── B.wav
├── C#.wav
├── D.wav
├── E.wav
├── F#.wav
├── requirements.txt   # Python dependencies
└── README.md          # This documentation

💻 Technologies Used
Library	Purpose	Version
OpenCV	Video capture and image processing 4.x
MediaPipe	Hand tracking and landmark detection	0.8.x
Pygame	Audio playback	2.x

🛠️ Installation
Clone the repository:

bash
git clone https://github.com/hellosound/ComputerVisionMusic.git
cd ComputerVisionMusic
Create virtual environment:

bash
python -m venv venv
venv\Scripts\activate  # Windows
Install dependencies:

bash
pip install opencv-python mediapipe pygame
🎮 Usage
Run the application:

bash
python main.py
Controls:

Show your hand to the webcam

Lower specific fingers to trigger sounds:

Index finger (A note)

Middle finger (B note)

Ring finger (D note)

Combinations trigger other notes

Press ESC to exit

🎥 Demonstration
https://youtu.be/SzGaMWH1qhE


📚 Code Explanation
Key Components:
Sound Initialization:

python
sounds = [
    pygame.mixer.Sound("A.wav"),
    pygame.mixer.Sound("B.wav"),
    ...
]
Finger Detection:

python
def is_finger_down(landmarks, finger_tip, finger_mcp):
    return landmarks[finger_tip].y > landmarks[finger_mcp].y
Main Processing Loop:

python
while cap.isOpened():
    # Capture frame
    # Process hand landmarks
    # Trigger sounds based on finger positions
📝 Note About Audio Files
The included WAV files are shared under [license type]. Please ensure you have proper rights to use these audio samples in your projects. Replace them with your own samples if needed.

🤝 Contributing
Contributions welcome! Please fork the repository and submit pull requests.

📜 License
MIT License


