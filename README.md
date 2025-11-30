🧠 Speech-to-Text System
👨‍💻 Internship Project — CodTech IT Solutions

Intern Name: Shreyash Nhanu Desai
Intern ID: CT04DR1291
Domain: Artificial Intelligence
Duration: 1st November – 1st December
Mentor: Neela Santosh

✅ Official Download Links (All Tools)
1️⃣ Download Python

🔗 Official Website:
https://www.python.org/downloads/

✔ Choose Python 3.9+ (64-bit)
✔ MUST check this during install: "Add Python to PATH"

2️⃣ Download Git

🔗 Official Website:
https://git-scm.com/downloads

✔ MUST check: "Add Git to PATH" during installation

3️⃣ Download FFmpeg

🔗 Official Download (Windows builds by Gyan):
https://www.gyan.dev/ffmpeg/builds/

➡ Download this ZIP: ffmpeg-gessentials.zip
➡ Extract → Rename to ffmpeg → Move to C:\
➡ Add to PATH:
C:\ffmpeg\bin

Verify:

ffmpeg -version

4️⃣ VS Code (Recommended IDE)

🔗 https://code.visualstudio.com/download

5️⃣ Python Libraries (Install After Everything)

Run this in CMD or VS Code terminal:

pip install torch transformers librosa soundfile ffmpeg-python sounddevice wavio

📘 Project Overview

This Speech-to-Text System converts audio into text using Wav2Vec2, a transformer-based model built by Facebook AI Research (FAIR).

It demonstrates AI skills in:

Deep Learning

Natural Language Processing

Audio Processing

Python Model Integration

🚀 Key Features (Simple Table)
Feature	Description
🎯 Accurate Speech Recognition	Converts speech → text with high accuracy
🤖 Wav2Vec2 Model	Uses facebook/wav2vec2-base-960h
🔌 Offline Mode	Works offline after initial download
🌍 Accent Support	Works well for clear English accents
💾 Auto Save	Saves transcript to output.txt
🔊 Audio Format	Requires mono 16kHz WAV
🛠️ Technologies Used
Category	Tools
Language	Python 3.9+
Framework	PyTorch
AI Model	Wav2Vec2
Audio	librosa, soundfile, ffmpeg
IDE	VS Code
Version Control	Git + GitHub
⚙️ System Requirements
Requirement	Description
Python	3.9+ 64-bit
Git	Must be on PATH
FFmpeg	Needed for audio conversion
RAM	Minimum 4GB recommended
🪜 Step-by-Step Installation (SUPER SIMPLE)
Step 1 — Install the Tools

Install Python → Add to PATH

Install Git → Add to PATH

Install FFmpeg → Add to PATH

Install VS Code

Step 2 — Download the Project
git clone https://github.com/ShreyashDesai/Speech-To-Text-System.git
cd Speech-To-Text-System

Step 3 — Install Python Libraries
pip install torch transformers librosa soundfile ffmpeg-python sounddevice wavio

🎤 Get Audio Samples (3 Easy Ways)
Option 1 — Windows Voice Recorder

Open Voice Recorder

Record

Save as sample.wav

Move into project folder

Option 2 — Convert MP3 → WAV
ffmpeg -i input.mp3 -ac 1 -ar 16000 sample.wav

Option 3 — Record Using Python
import sounddevice as sd
import wavio

duration = 5
fs = 16000

print("🎙️ Recording...")
audio = sd.rec(int(duration * fs), samplerate=fs, channels=1)
sd.wait()
wavio.write("sample.wav", audio, fs, sampwidth=2)
print("✅ Saved as sample.wav")


Install:

pip install sounddevice wavio

▶️ How to Run the Project
python speech_to_text.py --input sample.wav --output output.txt

📝 Example Output

Input Audio:
🎧 “Hello, this is my CodTech internship project.”

Output:

hello this is my codtech internship project

🧠 Model Information
Detail	Info
Model	facebook/wav2vec2-base-960h
Type	Transformer-based ASR
Made By	Facebook AI Research
Purpose	Speech-to-Text Conversion
👨‍💻 Author

Name: Shreyash Nhanu Desai
Role: AI Intern – CodTech IT Solutions
📧 Email: shreyashsn.desai@gmail.com

🔗 GitHub: https://github.com/ShreyashDesai

🔗 LinkedIn: https://linkedin.com/in/shreyash-desai-a13730384

🏁 Acknowledgements

Thanks to CodTech IT Solutions and Mentor Neela Santosh for support and guidance.

⚠️ Troubleshooting (Quick Fix Table)
Issue	Solution
pip not recognized	Install Python again → Check Add to PATH
git not recognized	Reinstall Git → Enable Add to PATH
ModuleNotFoundError	Run → pip install torch transformers
ffmpeg not found	Add C:\ffmpeg\bin to PATH
OSError -9996	Wrong microphone → select another device
