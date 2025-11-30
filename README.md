# 🧠 Speech-to-Text System
## 👨‍💻 Internship Project — CodTech IT Solutions

**Intern Name:** Shreyash Nhanu Desai  
**Intern ID:** CT04DR1291  
**Domain:** Artificial Intelligence  
**Duration:** 1st November – 1st December  
**Mentor:** Neela Santosh  

---

<div align="center"> 
<img width="100%" alt="Speech-to-Text System" src="https://github.com/user-attachments/assets/829776f9-82ea-4e41-8d6c-b3481698b43c" />
</div>

---

## 📘 Project Overview
The **Speech-to-Text System** is an AI-powered application that converts spoken audio into text using **Automatic Speech Recognition (ASR)**.  
It uses **Wav2Vec2**, a transformer-based deep learning model developed by **Facebook AI Research (FAIR)**.

This project demonstrates practical skills in:
- Deep Learning  
- Natural Language Processing (NLP)  
- Audio Signal Processing  
- Python Model Integration  

---

## 🚀 Key Features

| Feature | Description |
|--------|-------------|
| 🎯 Accurate Speech Recognition | High-precision speech-to-text conversion |
| 🤖 Wav2Vec2 Model | Uses facebook/wav2vec2-base-960h |
| 🔌 Offline Capability | Works offline after model download |
| 🌍 Accent Handling | Supports clear English and accents |
| 💾 Auto Save | Automatically saves to output.txt |
| 🔊 Audio Requirement | Only mono, 16kHz WAV supported |

---

## 🛠️ Technologies & Tools

| Category | Tools / Libraries |
|---------|-------------------|
| Language | Python 3.9+ |
| Framework | PyTorch |
| Model | Wav2Vec2 |
| Audio Processing | librosa, soundfile, ffmpeg |
| IDE | VS Code |
| Version Control | Git & GitHub |

---

# ⚙️ System Requirements

| Requirement | Description |
|------------|-------------|
| Python | Version 3.9+ (64-bit) |
| Git | Must be added to PATH |
| FFmpeg | Required for audio conversion |
| RAM | Minimum 4GB recommended |

---

# 📥 Installation Guide (Complete Step-by-Step)

## 1️⃣ Download & Install Required Software

### ✔ Python  
Download: https://www.python.org/downloads/  
➡ During installation → check **Add Python to PATH**

---

### ✔ Git  
Download: https://git-scm.com/downloads  
➡ During installation → check **Add Git to PATH**

---

### ✔ FFmpeg  
Download: https://www.gyan.dev/ffmpeg/builds/  
Choose: **ffmpeg-gessentials.zip**  
Extract → rename folder to **ffmpeg** → move to `C:\ffmpeg`

Add to PATH:
C:\ffmpeg\bin

makefile
Copy code

Verify:
ffmpeg -version

yaml
Copy code

---

### ✔ VS Code  
Download: https://code.visualstudio.com/download

---

## 2️⃣ Clone the GitHub Repository
```bash
git clone https://github.com/ShreyashDesai/Speech-To-Text-System.git
cd Speech-To-Text-System

--

3️⃣ Install Required Python Libraries
bash

pip install torch transformers librosa soundfile ffmpeg-python sounddevice wavio

--

🎤 Creating / Importing Audio
✅ Option 1 — Windows Voice Recorder
Open Voice Recorder

Record your audio

Save file as sample.wav

Move it into the project folder

--
✅ Option 2 — Convert MP3 to WAV (Mono, 16kHz)
bash
Copy code
ffmpeg -i input.mp3 -ac 1 -ar 16000 sample.wav

--
✅ Option 3 — Record Using Python
python
import sounddevice as sd
import wavio

duration = 5     # seconds
fs = 16000       # sample rate

print("🎙️ Recording...")
audio = sd.rec(int(duration * fs), samplerate=fs, channels=1)
sd.wait()
wavio.write("sample.wav", audio, fs, sampwidth=2)
print("✅ Saved as sample.wav")

--

▶️ How to Run the Speech-to-Text Program
bash
python speech_to_text.py --input sample.wav --output output.txt

--

📝 Example Output
Input:
🎧 sample.wav — “Hello, this is my CodTech internship project.”

Transcription Output:

text
Copy code
hello this is my codtech internship project
🧠 Model Information
Detail	Information
Model	facebook/wav2vec2-base-960h
Architecture	Transformer-based ASR
Developed By	Facebook AI Research (FAIR)
Purpose	Speech understanding & transcription

👨‍💻 Author
Name: Shreyash Nhanu Desai
Role: AI Intern — CodTech IT Solutions
📧 Email: shreyashsn.desai@gmail.com
🔗 GitHub: https://github.com/ShreyashDesai
🔗 LinkedIn: https://linkedin.com/in/shreyash-desai-a13730384

🏁 Acknowledgements
Special thanks to CodTech IT Solutions and Mentor Neela Santosh.

This project strengthened skills in:

Speech Recognition

Deep Learning Architectures

Transformer Models

Audio Processing

Python Model Deployment

⚠️ Troubleshooting Guide
Issue	Solution
pip not recognized	Reinstall Python → enable PATH
git not recognized	Reinstall Git → enable PATH
ModuleNotFoundError	Run: pip install torch transformers
ffmpeg not found	Add C:\ffmpeg\bin to PATH
OSError -9996	Change microphone / input device
Audio unreadable	Ensure WAV, mono, 16kHz format

