🧠 Speech-to-Text System
👨‍💻 Internship Project — CodTech IT Solutions

Intern Name: Shreyash Nhanu Desai
Intern ID: CT04DR1291
Domain: Artificial Intelligence
Duration: 1st November – 1st December (4 Weeks)
Mentor: Neela Santosh

<div align="center"> <img width="100%" alt="Speech-to-Text System" src="https://github.com/user-attachments/assets/829776f9-82ea-4e41-8d6c-b3481698b43c" /> </div>
📘 Project Overview

The Speech-to-Text System is an AI-powered application that converts spoken audio into text using Automatic Speech Recognition (ASR).
It utilizes Wav2Vec2, a state-of-the-art Transformer model by Facebook AI, known for its high accuracy in understanding raw audio signals.

This project was developed as part of my CodTech IT Solutions Internship under the Artificial Intelligence domain.
It demonstrates practical implementation of Deep Learning, NLP, and Audio Signal Processing.

🚀 Key Features
Feature	Description
🎯 Accurate Speech Recognition	Converts spoken words into precise text
🤖 Wav2Vec2 Model	Uses facebook/wav2vec2-base-960h
🔌 Offline Capability	Works offline after initial model download
🌍 Supports Multiple Accents	Optimized for clear English speech
💾 Auto Save	Saves output automatically to output.txt
🔊 Audio Support	Accepts mono 16kHz .wav files
🛠️ Technologies & Tools
Category	Tools / Libraries
Language	Python 3.9+
Deep Learning	PyTorch (torch)
Model	facebook/wav2vec2-base-960h
Audio Processing	librosa, soundfile, ffmpeg
IDE	VS Code (Recommended)
Version Control	Git & GitHub
⚙️ System Requirements
Requirement	Description
Python	Version 3.9+ (64-bit)
Git	Latest version added to PATH
FFmpeg	For audio conversion & preprocessing
VS Code	Recommended development environment
🪜 Installation & Setup Guide
Step 1️⃣ — Install Prerequisites
✔ Install Python

Enable: Add Python to PATH

✔ Install Git

Enable: Add Git to PATH

✔ Install FFmpeg

After installation, verify using:

ffmpeg -version

Step 2️⃣ — Clone the Repository
git clone https://github.com/ShreyashDesai/Speech-To-Text-System.git
cd Speech-To-Text-System

Step 3️⃣ — Install Required Libraries
pip install torch transformers librosa soundfile


If audio issues occur:

pip install ffmpeg-python

🎤 Creating or Importing Audio Samples

You will need a mono 16kHz WAV audio file.

Option 1 — Record Using Windows Voice Recorder

Open Voice Recorder

Record audio (e.g., “Hello, this is my CodTech internship project.”)

Save as sample.wav

Move it into your project folder

Option 2 — Convert MP3 to WAV
ffmpeg -i input.mp3 -ac 1 -ar 16000 sample.wav

Option 3 — Record Using Python
import sounddevice as sd
import wavio

duration = 5
fs = 16000

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

Transcribed Text:
🧾 hello this is my codtech internship project

🧠 Model Information
Detail	Information
Model Name	facebook/wav2vec2-base-960h
Architecture	Transformer-based ASR
Developed By	Facebook AI Research (FAIR)
Purpose	Speech representation & transcription
👨‍💻 Author

Name: Shreyash Nhanu Desai
Role: AI Intern, CodTech IT Solutions
Email: shreyashsn.desai@gmail.com

🔗 GitHub: https://github.com/ShreyashDesai
🔗 LinkedIn: linkedin.com/in/shreyash-desai-a13730384

🏁 Acknowledgements

Special thanks to CodTech IT Solutions and my mentor Neela Santosh for their continuous guidance and support throughout the internship.
This project enhanced my understanding of:

Speech Recognition

Deep Learning Architectures

Model Deployment

Audio Signal Processing

⚠️ Troubleshooting Guide
Issue	Solution
'pip' is not recognized	Reinstall Python & enable PATH
'git' is not recognized	Reinstall Git with PATH enabled
ModuleNotFoundError: torch	Install using pip install torch transformers
ffmpeg not found	Install FFmpeg & add to PATH
OSError: -9996 Invalid input device	Check microphone / select another audio device
