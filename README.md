# SpeechRecognition
This code can convert an audio file in .wav format to Text


import speech_recognition as sr
audio_file=("Audio.wav") # it is the audio file input
#use the audio file as source
r=sr.Recognizer()#initialize the recognizer
with sr.AudioFile(audio_file) as source:
    audio=r.record(source)#reads the audio file
try:
    print(" Audio file contains"+r.recognize_google(audio))
except sr.UnknownValueError:
    print("Google speech recognizer couldnot understand audio")
except sr.RequestError:
    print("Could not get result from google speech recognisation")    
     
