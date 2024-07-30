- [Install VLC](https://www.videolan.org/vlc/) or [ffmpeg](https://ffmpeg.org) (better the latter one)
- Convert a video (`.mp4` file) to an only audio (`.mp3` file)
	- Open VLC and go to `Media >> Converti/Salva`
	- Press `+ Aggiungi` and select the video you want to create subtitles for
	- Press `Converti/Salva`
	- The dot `Converti` must be selected
	- Change the `Profilo` to `Audio - MP3`
	- Select a new `Destinazione`
	- Press `Avvia`
- Go to [replicate.com](https://replicate.com/m1guelpf/whisper-subtitles) drop the audio into the `audio path` and press `submit`
- If you want to create ***NOTES*** for them (***IT DOES NOT WORK!***): %% fold %%
  1. Go to [promt splitter](https://chatgpt-prompt-splitter.jjdiaz.dev) and pass the whole subtitle text
  2. Pass each "split" to ChatGPT.
  3. Ask him somenting like: ***The parts I passed you previously are subtitles taken from a single lecture of "Sensor and Microsystems", can you make COMPREHENSIVE and COMPLETE notes for me, given those subtitles and your extensive knowledge on the subject***
  4. If there are formulas you can ask for a Latex formatting in this way: ***If you write any equation do it in this format `$$ <latex code here> $$`***