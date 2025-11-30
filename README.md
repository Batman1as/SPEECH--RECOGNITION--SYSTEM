# 🎤 Speech-To-Text System (Wav2Vec2)

This project converts human speech into text using the **Wav2Vec2 transformer model**.

---

## 2️⃣ Clone the GitHub Repository

```bash
git clone https://github.com/ShreyashDesai/Speech-To-Text-System.git
cd Speech-To-Text-System
3️⃣ Install Required Python Libraries
bash
Copy code
pip install torch transformers librosa soundfile ffmpeg-python sounddevice wavio
🎧 Creating / Importing Audio
✅ Option 1 — Windows Voice Recorder
Open Voice Recorder

Record your audio

Save file as sample.wav

Move it into the project folder

✅ Option 2 — Convert MP3 to WAV (Mono, 16kHz)
bash
Copy code
ffmpeg -i input.mp3 -ac 1 -ar 16000 sample.wav
✅ Option 3 — Record Audio Using Python
python
Copy code
import sounddevice as sd
import wavio

duration = 5
fs = 16000

print("🎙️ Recording...")
audio = sd.rec(int(duration * fs), samplerate=fs, channels=1)
sd.wait()
wavio.write("sample.wav", audio, fs, sampwidth=2)
print("✅ Saved as sample.wav")
▶️ Running the Speech-to-Text Program
bash
Copy code
python speech_to_text.py --input sample.wav --output output.txt
📝 Example Output
Input audio: “Hello, this is my CodTech internship project.”

Transcribed text:

text
Copy code
hello this is my codtech internship project
🧠 Model Information
Detail	Information
Model	facebook/wav2vec2-base-960h
Type	Transformer-based ASR
Developer	Facebook AI Research
Purpose	Speech Recognition

👤 Author
Name: Shreyash Nhanu Desai
Role: AI Intern – CodTech IT Solutions
📧 Email: shreyashsn.desai@gmail.com
🔗 GitHub: https://github.com/ShreyashDesai
🔗 LinkedIn: https://linkedin.com/in/shreyash-desai-a13730384

🏁 Acknowledgements
Special thanks to CodTech IT Solutions and Mentor Neela Santosh for guidance through this internship.

This project improved skills in:

Speech Recognition

Audio Preprocessing

Transformers

Deep Learning

Deployment using Python

⚠️ Troubleshooting Guide
Issue	Fix
pip not recognized	Reinstall Python & enable PATH
git not recognized	Install Git & enable PATH
Module import errors	Run pip install -r requirements.txt
ffmpeg not found	Add C:\ffmpeg\bin to PATH
Wrong audio format	Use WAV, mono, 16kHz

yaml
Copy code

