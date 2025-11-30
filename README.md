🧠 Speech-to-Text System using Wav2Vec2
Internship Project – CodTech IT Solutions
Intern Name: Shreyash Nhanu Desai
Intern ID: CT04DR1291
Domain: Artificial Intelligence
Duration: 1st November – 1st December 2025
Mentor: Neela Santosh

  Speech-to-Text Banner
  




📘 Project Overview
A complete, offline, and easy-to-run Speech-to-Text (STT) system built using Facebook's Wav2Vec2 model (facebook/wav2vec2-base-960h).
This project is designed to be beginner-friendly, fully functional out-of-the-box, and requires zero manual configuration after following the steps below.

🚀 Key Features





































FeatureDescriptionHigh AccuracyUses pre-trained Wav2Vec2 (960h LibriSpeech)100% OfflineWorks without internet after first downloadSimple CLIOne command to transcribe any WAV fileAuto ResamplingAutomatically converts any audio to 16kHz monoLive Microphone RecordingBuilt-in recorder (just press Enter)Auto-save transcriptionSaves to output.txt automaticallyCross-platformWindows / macOS / Linux

🛠 Technologies Used





























CategoryTools / LibrariesLanguagePython 3.9+Deep LearningPyTorch + Hugging Face TransformersModelfacebook/wav2vec2-base-960hAudio Processinglibrosa, torchaudio, soundfile, sounddevice, pydubPackagingrequirements.txt

📥 Super Easy Installation (One-Click Setup)
Step 1: Install Required Software (Only once)

























SoftwareDownload LinkImportant StepPython 3.11https://www.python.org/downloads/✅ Check "Add to PATH"Githttps://git-scm.com/downloads✅ Check "Add to PATH"FFmpeghttps://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.zipExtract → Add bin folder to PATH
How to add FFmpeg to PATH (Windows):
Extract zip → rename folder to ffmpeg
Move to C:\ffmpeg
Add C:\ffmpeg\bin to System PATH
Restart terminal → type ffmpeg -version to verify

Step 2: Clone & Setup Project (3 commands only)
Bashgit clone https://github.com/ShreyashDesai/Speech-To-Text-System.git
cd Speech-To-Text-System
pip install -r requirements.txt
First run will download the Wav2Vec2 model (~360 MB) automatically.

🎤 How to Use (3 Ways)
Option 1: Transcribe Existing Audio File
Bashpython stt.py your_audio.mp3
# or
python stt.py recording.wav
Supports: .wav, .mp3, .m4a, .flac, etc.
Option 2: Record from Microphone (Live)
Bashpython stt.py --record
→ Press Enter when ready → Speak → Press Enter again to stop
→ Transcription appears instantly!
Option 3: Use Default sample.wav
Bashpython stt.py
Uses sample.wav in the folder (already included)
Output is automatically saved to output.txt

📁 Project Structure
textSpeech-To-Text-System/
├── stt.py                  ← Main script (single file!)
├── requirements.txt
├── sample.wav              ← Demo audio
├── output.txt              ← Auto-saved transcription
├── README.md
└── assets/                 ← Images

⚡ The Only Code File You Need – stt.py (Copy-Paste Ready)
Python# stt.py - Easy Speech-to-Text using Wav2Vec2
# Author: Shreyash Nhanu Desai

import torch
from transformers import Wav2Vec2ForCTC, Wav2Vec2Processor
import librosa
import sounddevice as sd
import wavio
import argparse
import os
from pydub import AudioSegment
import sys

# Load model and processor (auto downloads on first run)
print("🔄 Loading Wav2Vec2 model...")
processor = Wav2Vec2Processor.from_pretrained("facebook/wav2vec2-base-960h")
model = Wav2Vec2ForCTC.from_pretrained("facebook/wav2vec2-base-960h")
print("✅ Model loaded successfully!\n")

def load_audio(file_path):
    """Load any audio and convert to 16kHz mono WAV"""
    if not os.path.exists(file_path):
        print(f"❌ File not found: {file_path}")
        sys.exit(1)
    
    print(f"🔄 Loading and converting: {file_path}")
    audio = AudioSegment.from_file(file_path)
    audio = audio.set_channels(1).set_frame_rate(16000)
    temp_wav = "temp_input.wav"
    audio.export(temp_wav, format="wav")
    
    speech, sr = librosa.load(temp_wav, sr=16000)
    os.remove(temp_wav)
    return speech

def record_audio(duration=8):
    """Record from microphone"""
    print(f"🎙️  Recording for {duration} seconds... (Press Ctrl+C to stop early)")
    fs = 16000
    recording = sd.rec(int(duration * fs), samplerate=fs, channels=1, dtype='float32')
    sd.wait()
    wavio.write("recorded.wav", recording, fs, sampwidth=2)
    print("✅ Recording saved as recorded.wav")
    return recording.flatten()

def transcribe(speech):
    input_values = processor(speech, return_tensors="pt", sampling_rate=16000).input_values
    logits = model(input_values).logits
    predicted_ids = torch.argmax(logits, dim=-1)
    transcription = processor.decode(predicted_ids[0])
    return transcription.lower()

def main():
    parser = argparse.ArgumentParser(description="Easy Speech-to-Text using Wav2Vec2")
    parser.add_argument("file", nargs="?", default="sample.wav", help="Audio file path")
    parser.add_argument("--record", action="store_true", help="Record from microphone")
    args = parser.parse_args()

    if args.record:
        print("🎤 Microphone mode activated!")
        speech = record_audio(duration=10)
        print("🔄 Transcribing...")
    else:
        speech = load_audio(args.file)
        print("🔄 Transcribing...")

    text = transcribe(speech)
    print("\n" + "="*50)
    print("📝 TRANSCRIPTION:")
    print("="*50)
    print(text)
    print("="*50)

    # Auto-save
    with open("output.txt", "w", encoding="utf-8") as f:
        f.write(text)
    print("\n💾 Saved to output.txt")

if __name__ == "__main__":
    main()

✅ requirements.txt (Copy this exactly)
txttorch>=2.0.0
transformers
librosa
sounddevice
wavio
pydub
ffmpeg-python

🏆 Demo Output Example
textInput: "Hello, this is my CodTech internship project on speech recognition."
Output (saved in output.txt):
hello this is my codtech internship project on speech recognition

🙏 Acknowledgements
Huge thanks to:

CodTech IT Solutions
Mentor: Neela Santosh
Hugging Face & Facebook AI Research (Wav2Vec2)


👤 Author
Shreyash Nhanu Desai
AI Intern | Passionate about NLP & Audio AI
📧 shreyashsn.desai@gmail.com
🔗 GitHub: https://github.com/ShreyashDesai
🔗 LinkedIn: https://linkedin.com/in/shreyash-desai-a13730384
