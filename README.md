# How-to-Remove-Vocals-from-a-Song
This file is concerned about the experience how I removed vocals from a song by spleeter.

I just don't want to forget the process.

This is a memorandum for myself, which might help others.

## Install Python
The latest version may not be compatible with spleeter up to now(2022.3.24). I used Python 3.8.0 and it worked.

## Install spleeter
Run Windows PowerShell.

Use `pip install spleeter` to install spleeter.

## Install FFmpeg
Install FFmpeg from [ffmpeg.org](https://ffmpeg.org).

## Install ffmpeg-python
I came across some problems. I solved them by the way below.

`pip uninstall ffmpeg`

`pip uninstall ffmpeg-python`

`pip install ffmpeg-python`

## Remove Vocals from Song
Run `spleeter separate 'the_song_from_which_you_want_to_remove_vocals.mp3' -p spleeter:2stems -o 'the_directory_to_which_you_want_to_save_the_results` in Windows PowerShell.

I came across problems with librosa and resampy. I used the commands below to solve it.

`pip uninstall librosa`

`pip install librosa==0.8.0`

`pip uninstall resampy`

`pip install resampy`

## Success
`spleeter separate 'the_song_from_which_you_want_to_remove_vocals.mp3' -p spleeter:2stems -o 'the_directory_to_which_you_want_to_save_the_results`

Congrats! I succeeded although the results weren't good.
