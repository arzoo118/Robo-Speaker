#PROJECT 1
# ULTRA ROBO SPEAKER

!pip install gtts

from gtts import gTTS as g

from IPython.display import Audio, display

def t_t_s(text):
    tts = g(text)
    tts.save("say.mp3")
    return "say.mp3"

def play_audio(file_path):
    display(Audio(file_path, autoplay=True))

print("WELCOME TO ULTRA ROBO SPEAKER BY MUNTAZIR")
while True:
  text = input("ENTER A TEXT :")
  if text == "z":
    say = t_t_s("bye bye")
    play_audio(say)
    break
  say = t_t_s(text)
  play_audio(say)
