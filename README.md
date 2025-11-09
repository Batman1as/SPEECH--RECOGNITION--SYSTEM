# 🧠 SPEECH-TO-TEXT SYSTEM

### 👨‍💻 Company: CodTech IT Solutions  
**Name:** Shreyash Nhanu Desai  
**Intern ID:** CT04DR1291  
**Domain:** Artificial Intelligence  
**Duration:** 4 Weeks  
**Mentor:** Neela Santosh  

---

<img width="1873" height="495" alt="Speech-to-Text System" src="https://github.com/user-attachments/assets/829776f9-82ea-4e41-8d6c-b3481698b43c" />

---

## 📘 Project Overview

The **Speech-to-Text System** is an AI-powered project that converts spoken audio into written text using advanced deep learning models.  
It demonstrates the power of **Automatic Speech Recognition (ASR)** through the **Wav2Vec2 Transformer model** by Facebook AI.

This project was developed as part of my **CodTech Internship** (AI Domain) and showcases practical applications of **NLP + Audio Processing** using Python and Transformers.

---

## 🚀 Features

- 🎤 Converts voice (WAV audio) into accurate text  
- ⚙️ Uses **Wav2Vec2**, a state-of-the-art speech recognition model  
- 💬 Works offline after model download  
- 🧩 Supports multiple accents and clear speech  
- 💾 Saves transcription results automatically to `output.txt`  
- 🔊 Accepts short audio clips in mono 16kHz WAV format  

---

## 🛠️ Technologies Used

**Programming Language:** Python  

**Libraries Used:**
- `transformers` – for pre-trained Wav2Vec2 model  
- `torch` – deep learning backend  
- `librosa` – audio loading and resampling  
- `soundfile` – for audio file handling  

---

## ⚙️ System Requirements & Installation Checklist

Before running the project, ensure you have these installed 👇  

### 🪜 Step 0 — Prerequisites

1. **Python 3.9+ (64-bit)**  
   👉 [Download Python](https://www.python.org/downloads/)  
   ✅ During setup: check **“Add Python to PATH”**

2. **Git (64-bit)**  
   👉 [Download Git](https://git-scm.com/downloads)  
   ✅ During setup: check **“Add Git to PATH”**

3. **FFmpeg** (for audio format conversion)  
   👉 [Download FFmpeg](https://ffmpeg.org/download.html)  
   ✅ Add it to your system PATH and verify:  
   ```bash
   ffmpeg -version
VS Code (recommended)
👉 Download VS Code

💻 How to Run
1️⃣ Clone this repository
bash
Copy code
git clone https://github.com/Batman1as/Speech-To-Text-System.git
cd Speech-To-Text-System
2️⃣ Install dependencies
bash
Copy code
pip install torch transformers librosa soundfile
(Optional: if ffmpeg or audio issues occur)

bash
Copy code
pip install ffmpeg-python
🎤 How to Create a sample.wav File
Before running the script, you’ll need an audio file to test your model.

🪄 Option 1 — Record using Windows Voice Recorder
Open Voice Recorder app.

Record a short clip (e.g. “Hello, this is my CodTech internship project.”)

Save it, rename it to sample.wav, and move it to your project folder.

⚙️ Option 2 — Convert MP3 to WAV
bash
Copy code
ffmpeg -i input.mp3 -ac 1 -ar 16000 sample.wav
🧠 Option 3 — Record inside Python
python
Copy code
import sounddevice as sd
import wavio

duration = 5  # seconds
fs = 16000    # sample rate

print("🎙️ Recording...")
recording = sd.rec(int(duration * fs), samplerate=fs, channels=1)
sd.wait()
wavio.write("sample.wav", recording, fs, sampwidth=2)
print("✅ Saved as sample.wav")
To install:

bash
Copy code
pip install sounddevice wavio
3️⃣ Run the script
bash
Copy code
python speech_to_text.py --input sample.wav --output output.txt
4️⃣ Check output
Your transcription will be displayed in the terminal and saved in output.txt.

🧩 Example Output
Input Audio:
🎧 sample.wav — “Hello, this is my CodTech internship project.”

Output Text:
📝 hello this is my codtech internship project

🧠 Model Information
Model Used: facebook/wav2vec2-base-960h

About:
Wav2Vec2 is a Transformer-based model by Facebook AI that learns speech representations directly from raw audio.
It delivers high accuracy in recognizing and transcribing human speech efficiently.

👨‍💻 Author
Shreyash Desai
Intern at CodTech IT Solutions

📧 Email: shreyashsn.desai@gmail.com
🔗 GitHub: https://github.com/Batman1as
🔗 LinkedIn: https://www.linkedin.com/in/shreyash-desai-a13730384/

🏁 Acknowledgements
A heartfelt thanks to CodTech IT Solutions and Mentor Neela Santosh
for their constant guidance, support, and valuable learning experience during this internship.

⚠️ Troubleshooting
Issue	Fix
'pip' is not recognized	Reinstall Python and check “Add Python to PATH”
'git' is not recognized	Reinstall Git (64-bit) and check “Add Git to PATH”
ModuleNotFoundError: No module named 'torch'	Run pip install torch transformers
ffmpeg not found	Install FFmpeg and add to PATH
OSError: [Errno -9996] Invalid input device	Check your microphone or try a different one

⭐ If you found this project helpful, don’t forget to star the repository!
