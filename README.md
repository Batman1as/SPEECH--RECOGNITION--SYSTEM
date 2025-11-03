🧠 SPEECH-TO-TEXT SYSTEM

Company: CodTech IT Solutions

Name: Shreyash Nhanu Desai

Intern ID: CT04DR1291

Domain: Artificial Intelligence

Duration: 4 Weeks

Mentor: Neela Santosh

--

<img width="1873" height="495" alt="Speech-to-Text System" src="https://github.com/user-attachments/assets/829776f9-82ea-4e41-8d6c-b3481698b43c" />
--
📘 Project Overview

The Speech-to-Text System is an AI-based project that converts spoken audio into written text using pre-trained deep learning models.
It demonstrates how modern Automatic Speech Recognition (ASR) models understand human speech and accurately generate transcriptions.

This project is part of my CodTech Internship (AI Domain) and showcases practical use of NLP + Audio Processing with Transformers.
--
🚀 Features

🎤 Converts voice (WAV audio) into accurate text
⚙️ Uses Wav2Vec2, a state-of-the-art speech recognition model
💬 Works completely offline after model download
🧩 Supports multiple accents and clear speech
💾 Saves transcription results automatically into a file (output.txt)
🔊 Accepts short audio clips in mono 16kHz WAV format
--
🛠️ Technologies Used

Programming Language: Python

Libraries:

transformers – For the Wav2Vec2 model

torch – Deep learning backend

librosa – Audio loading and resampling

soundfile – Audio file support
--
💻 How to Run
1️⃣ Clone this repository
git clone https://github.com/Batman1as/Speech-To-Text-System.git
cd Speech-To-Text-System
--
2️⃣ Install dependencies
pip install torch transformers librosa soundfile
--
3️⃣ Prepare your audio file

Convert to mono, 16kHz WAV using ffmpeg (if needed):

ffmpeg -i input.mp3 -ac 1 -ar 16000 sample.wav
--
4️⃣ Run the script
python speech_to_text.py --input sample.wav --output output.txt
--
5️⃣ Check output

Your transcription will be displayed on screen and saved in output.txt.
--
🧩 Example Output

Input:
🎧 sample.wav — “Hello, this is my CodTech internship project.”
--
Output:
📝 hello this is my codtech internship project
--
🧠 Model Information

Model: facebook/wav2vec2-base-960h

Wav2Vec2 is a Transformer-based model developed by Facebook AI for Automatic Speech Recognition (ASR).
It learns speech representations directly from raw audio data and transcribes speech efficiently and accurately.

👨‍💻 Author

Shreyash Desai
Intern at CodTech IT Solutions

📧 [shreyashsn.desai@gmail.com
]
🔗 GitHub Profile https://github.com/Batman1as
--
🔗 LinkedIn Profile https://www.linkedin.com/in/shreyash-desai-a13730384/ linkedin
--

🏁 Acknowledgements

I would like to thank CodTech IT Solutions and my mentor Neela Santosh for providing this opportunity, guidance, and valuable learning experience during my internship.


