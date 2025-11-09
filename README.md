🧠 Speech-to-Text System
👨‍💻 Internship Project — CodTech IT Solutions

Intern Name: Shreyash Nhanu Desai
Intern ID: CT04DR1291
Domain: Artificial Intelligence
Duration: 1st November – 1st December (4 Weeks)
Mentor: Neela Santosh

<div align="center"> <img width="100%" alt="Speech-to-Text System" src="https://github.com/user-attachments/assets/829776f9-82ea-4e41-8d6c-b3481698b43c" /> </div>
📘 Project Overview

The Speech-to-Text System is an AI-powered application that converts human speech into text using Automatic Speech Recognition (ASR).
It leverages Wav2Vec2, a cutting-edge Transformer model developed by Facebook AI, to deliver highly accurate transcriptions from raw audio input.

This project was completed as part of my CodTech IT Solutions Internship under the Artificial Intelligence domain.
It demonstrates practical applications of Deep Learning, Natural Language Processing (NLP), and Audio Signal Processing using Python.

🚀 Key Features

✅ Converts audio speech into precise text output
✅ Powered by Wav2Vec2 – a state-of-the-art transformer model
✅ Works offline after initial model download
✅ Supports clear English speech and multiple accents
✅ Automatically saves transcription to output.txt
✅ Accepts mono 16kHz .wav audio files for best results

🛠️ Technologies & Tools
Category	Tools / Libraries
Language	Python 3.9+
Deep Learning	PyTorch (torch)
Model	facebook/wav2vec2-base-960h
Audio Processing	librosa, soundfile, ffmpeg
Environment	VS Code (Recommended)
Version Control	Git & GitHub
⚙️ System Requirements
Requirement	Description
Python	Version 3.9 or higher (64-bit)
Git	Latest version with PATH enabled
FFmpeg	For audio conversion and preprocessing
VS Code	Recommended IDE for running the project
🪜 Installation & Setup Guide
Step 1️⃣ — Install Prerequisites

Download Python

✅ During installation, check “Add Python to PATH”

Download Git

✅ Enable “Add Git to PATH”

Download FFmpeg

✅ Add FFmpeg to your PATH

ffmpeg -version

Step 2️⃣ — Clone the Repository
git clone https://github.com/ShreyashDesai/Speech-To-Text-System.git
cd Speech-To-Text-System

Step 3️⃣ — Install Required Libraries
pip install torch transformers librosa soundfile


If you face audio-related issues, also install:

pip install ffmpeg-python

🎤 Creating or Importing Audio Samples

You’ll need a .wav file recorded at 16kHz (mono).

Option 1 — Record Using Windows Voice Recorder

Open Voice Recorder app

Record a short clip (e.g. “Hello, this is my CodTech internship project.”)

Save it as sample.wav and place it in your project folder

Option 2 — Convert MP3 to WAV
ffmpeg -i input.mp3 -ac 1 -ar 16000 sample.wav

Option 3 — Record Using Python
import sounddevice as sd
import wavio

duration = 5  # seconds
fs = 16000    # sample rate

print("🎙️ Recording...")
recording = sd.rec(int(duration * fs), samplerate=fs, channels=1)
sd.wait()
wavio.write("sample.wav", recording, fs, sampwidth=2)
print("✅ Saved as sample.wav")


Install dependencies:

pip install sounddevice wavio

▶️ How to Run
python speech_to_text.py --input sample.wav --output output.txt

📝 Example Output

Input Audio:
🎧 sample.wav — “Hello, this is my CodTech internship project.”

Output Text:
🧾 hello this is my codtech internship project

🧠 Model Information

Model Name: facebook/wav2vec2-base-960h

Architecture: Transformer-based ASR model

Developed By: Facebook AI Research (FAIR)

Purpose: Learn speech representations directly from raw audio signals for transcription and language understanding tasks.

👨‍💻 Author

Name: Shreyash Nhanu Desai
Role: AI Intern at CodTech IT Solutions
Email: shreyashsn.desai@gmail.com

GitHub: github.com/Batman1as

LinkedIn: linkedin.com/in/shreyash-desai-a13730384

🏁 Acknowledgements

A heartfelt thanks to CodTech IT Solutions and Mentor Neela Santosh for their guidance, mentorship, and invaluable support throughout the internship.
This project enhanced my understanding of Speech Recognition, Deep Learning Models, and Practical AI Deployment.

⚠️ Troubleshooting Guide
Issue	Possible Fix
'pip' is not recognized	Reinstall Python and enable Add to PATH
'git' is not recognized	Reinstall Git (64-bit) and enable Add to PATH
ModuleNotFoundError: No module named 'torch'	Run pip install torch transformers
ffmpeg not found	Install FFmpeg and add to PATH
OSError: [Errno -9996] Invalid input device	Check microphone connection or select another input device
⭐ Support

If you found this project useful, please consider giving it a ⭐ on GitHub!
