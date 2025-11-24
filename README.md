Voice Assistant (Siri/Alexa Clone)

This project is a simple Python-based voice assistant capable of listening to user commands, speaking responses, searching Wikipedia, telling jokes, reporting the time, and opening basic applications.
It uses offline text-to-speech and online Google Speech Recognition for speech-to-text.

⸻

Features
	•	Wake-word activation (“assistant”)
	•	Speech-to-text using Google STT
	•	Offline text-to-speech using pyttsx3
	•	Wikipedia search
	•	Time reporting
	•	Telling jokes
	•	Opening local applications (Notepad, Calculator)
	•	Simple extensible command handler

⸻

Project Structure

voice-assistant/
│
├── assistant.py
├── commands.py
├── requirements.txt
└── README.md


⸻

Installation
	1.	Install Python 3.9 or higher.
	2.	Install system dependencies:

Windows:

pip install pipwin
pipwin install pyaudio

Linux:

sudo apt install portaudio19-dev python3-pyaudio

Mac:

brew install portaudio

	3.	Install project dependencies:

pip install -r requirements.txt


⸻

Requirements

SpeechRecognition
pyttsx3
pyaudio
wikipedia


⸻

Usage

Run the assistant:

python assistant.py

The assistant will start and say:

Hello! Say 'assistant' to wake me up.

After that, say:
	•	“assistant” (wake word)
	•	“what time is it”
	•	“search machine learning”
	•	“tell me a joke”
	•	“open notepad”
	•	“goodbye”

⸻

How It Works

Wake Word

The program continuously listens for the keyword “assistant.” Once detected, it activates command mode.

Speech Recognition

The SpeechRecognition library processes microphone audio and uses Google STT to convert speech to text.

Text-to-Speech

pyttsx3 provides offline TTS to speak responses.

Command Processing

The command handler interprets user input and calls functions located in commands.py.

⸻

Extending the Assistant

You can add new commands inside commands.py.

Example:

def weather():
    return "The weather feature is not implemented yet."

Then connect it in assistant.py inside handle_command():

elif "weather" in cmd:
    speak(weather())


⸻

Troubleshooting

Microphone Not Working

Ensure your microphone is selected as the default input device on your OS.

PyAudio Installation Errors

Install PortAudio first, then PyAudio using pipwin (Windows) or brew/apt (macOS/Linux).

Wikipedia Errors

Some queries may return disambiguation errors. Try more specific search terms.

⸻

License

This project is provided for educational and personal use. You may modify, distribute, or integrate it into your own applications.

⸻

