So this is how to run these files:
get the following dependencies
# Core Dependencies
flask==3.0.2
werkzeug==3.0.1
PyPDF2==3.0.1
SpeechRecognition==3.10.1
pyttsx3==2.90
gTTS==2.5.1
pygame==2.5.2
pyaudio==0.2.14
requests==2.31.0
python-dotenv==1.0.1

# External Requirements
- Ollama (must be installed and running)
- gemma2:2b model (install via: ollama pull gemma2:2b)

once it is done, run the app.py in *Thinking* folder

Thinking Folder: this is where u upload the resume and it uses the model to get questions using the LLM. This LLM response can be changed as we please by changing the prompt in the source code.

then make sure u close the first app or it keeps throwing an error and then run the app.py in talking folder

Talking Folder: This folder user pygame to read the questions aloud and record responses. I have added buttons because it was much harder to control the questions timings without them.

once this is done the questions and the answers will be stored in a json file in the shared_questions folder.

Once all this is one, run the interview_analyzer.py in the final folder. this makes the model analyze the responses and then read aloud the response of the model telling if they are selected or not.
