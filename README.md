# Speech-Recognition-Google-Speech-API-Python
How speech recognition can be done using Python, Google's Speech API, and ReSpeaker USB Mic.

Speech Recognition

Speech Recognition is a part of Natural Language Processing which is a subfield of Artificial Intelligence. To put it simply, speech recognition is the ability of a computer software to identify words and phrases in spoken language and convert them to human readable text. It is used in several applications such as voice assistant systems, home automation, voice based chatbots, voice interacting robot, artificial intelligence and etc.

There are different APIs(Application Programming Interface) for recognizing speech. They offer services either free or paid. These are:

CMU Sphinx
Google Speech Recognition
Google Cloud Speech API
Wit.ai
Microsoft Bing Voice Recognition
Houndify API
IBM Speech To Text
Snowboy Hotword Detection
We will be using Google Speech Recognition here, as it doesn't require any API key. This project aims to provide an introduction on how to use Google Speech Recognition library on Python with the help of external microphone like ReSpeaker USB 4-Mic Array from Seeed Studio. Although it is not mandatory to use external microphone, even built-in microphone of laptop can be used.

ReSpeaker USB 4-Mic Array
The ReSpeaker USB Mic is a quad-microphone device designed for AI and voice applications, which was developed by Seeed Studio. It has 4 high performance, built-in omnidirectional microphones designed to pick up your voice from anywhere in the room and 12 programmable RGB LED indicators. The ReSpeaker USB mic supports Linux, macOS, and Windows operating systems.

![image](https://user-images.githubusercontent.com/67792642/120223594-59295880-c231-11eb-874a-ab954b13c29f.png)

![image](https://user-images.githubusercontent.com/67792642/120223645-6fcfaf80-c231-11eb-824f-b7ce934b5317.png)

The ReSpeaker USB Mic comes in a nice package containing the following items:

A user guide
 ReSpeaker USB Mic Array
Micro USB to USB Cable

![image](https://user-images.githubusercontent.com/67792642/120223734-9392f580-c231-11eb-9c1b-6f6c8e39e65d.png)

So we're ready to get started.

Install Required Libraries
For this project, I’ll assume you are using Python 3.x.

Let's install the libraries:

pip3 install SpeechRecognition
For macOS, first you will need to install PortAudio with Homebrew, and then install PyAudio with pip3:

brew install portaudio
pip3 install pyaudio
For Linux, you can install PyAudio with apt:

sudo apt-get install python-pyaudio python3-pyaudio
For Windows, you can install PyAudio with pip:

pip install pyaudio
Create a new python file 

nano get_index.py
Paste on get_index.py
Run the following command:

python3 get_index.py
In my case, command gives following output to screen :

Input Device id 1 - ReSpeaker 4 Mic Array (UAC1.0)
Input Device id 2 - MacBook Air Microphone
Change device_index to index number as per your choice in below code snippet.

Run the following command:

python3 get_index.py
In my case, command gives following output to screen :

Input Device id 1 - ReSpeaker 4 Mic Array (UAC1.0)

Input Device id 2 - MacBook Air Microphone
Text-to-speech in Python With pyttsx3 Library
There are several APIs available to convert text to speech in python. One of such APIs is the pyttsx3, which is the best available text-to-speech package in my opinion. This package works in Windows, Mac, and Linux. Check the official documentation to see how this is done.

Install the package

Use pip to install the package.

pip install pyttsx3
If you are in Windows, you will need an additional package, pypiwin32 which it will need to access the native Windows speech API.

pip install pypiwin32
Convert text to speech python script
Putting It All Together
The below code for recognising human speech using Google Speech Recognition, and converting the text into speech using pyttsx3 library is put_together.py
It prints output on terminal. Also, it will be converted into speech as well.

You said: London is the capital of Great Britain
