

Suggested updated `README.md` with two small, repository-supported improvements: correct the command-line entry point to `pysync/__main__.py`, and note that the first run downloads the Whisper `medium` model.

```markdown
# Sync Lyrics and Produce an LRC file using spleeter, whisper, and text similarity.

## Installation

Install [Anaconda3](https://www.anaconda.com/download) and open the Anaconda Prompt.

1. Move to your Projects directory. (You can switch drive letters by just entering e.g. `F:` and hitting enter for the drive letter F.)
2. Create an environment: `conda create --name lyrics python=3.10.12`
3. Activate the environment: `conda activate lyrics`
4. Install `whisper` and `spleeter`: `pip install spleeter openai-whisper`
5. Download [ffmpeg](https://ffmpeg.org/download.html) and put the ffmpeg.exe into your project directory within Anaconda (Seems like having it in PATH doesn't work on windows...)

Now you're good to go, just execute it from within Anaconda Prompt. Every time you close the Anaconda Prompt you should repeat step 1 and 3 before executing the script.

## Usage

Pysync can be used using the command line. Setup the environment using conda and make sure that `whisper` and `spleeter` are installed. Then you can use this via the command line, providing an mp3 of the song and text file with lyrics you want to sync. The program will produce a .lrc file with timestamps which can be used by various lyric display programs.

Run it from the repository root:

`python pysync/__main__.py [-h] [--output_file OUTPUT_FILE] music lyrics`

Example:

`python pysync/__main__.py song.mp3 lyrics.txt`

The first run will download the Whisper `medium` model.
```
