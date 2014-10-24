spectrogram
===========

This GUI program can generate spectrograms from sound files and synthesize spectrograms back into sound (with large loss of fidelity).

The program can be built on Linux or you can use the Windows binary (bin/spectrogram.exe).  The program was a part of my 2010 bachelor's thesis and there will be no more development.  It was inspired heavily by the ARSS program: http://arss.sourceforge.net/

![screenshot](http://krajj7.github.io/spectrogram/spectrogram.png)

## Spectrogram examples

Some example spectrograms of classical music made with this program can be found on my youtube channel:

https://www.youtube.com/watch?v=Txp-pHU2K6w

https://www.youtube.com/watch?v=XJ6XXjAOvmY

https://www.youtube.com/watch?v=bGtup1qCHW0

There are no demos of the synthesis functionality (sound from spectrogram), but it works a lot like this: http://arss.sourceforge.net/examples.shtml

### How to make a video spectrogram like the examples

To turn the spectrogram image generated by this program into a video there is a quick & dirty script in python (scripts/spectrogram-video.py) to generate each frame as a png file (takes quite long and makes many files) and then you can use this ffmpeg command (on Linux) to put it together into a video with sound (example for 25 fps): 

 `ffmpeg -f image2 -r 25 -i ./%06d.png -i soundfile.mp3 -b 5000k -vb 5000k -acodec copy out.mp4`

## Documentation

At http://krajj7.github.io/spectrogram
