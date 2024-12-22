# Real Time Whisper Transcription

![Demo gif](demo.gif)

This is a demo of real time speech to text with OpenAI's Whisper model. It works by constantly recording audio in a thread and concatenating the raw bytes over multiple recordings.

## Installation

### Environment Setup

Some of the packages aren't compatible with the newest version of python.

I recommend starting with pyenv to install python 3.11

```
pyenv install 3.11.5
pyenv local 3.11.5
python --version 
```

If that comes back with anything other than 3.11, make sure you add this to your aliases and source them, or run this directly in your terminal.

```
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
```

Set up a virtual env with
```
python -m venv env
source env/bin/activate
```

### Package Installation

Then, to install dependencies simply run
```
pip install -r requirements.txt
```
in an environment of your choosing.

Whisper also requires the command-line tool [`ffmpeg`](https://ffmpeg.org/) to be installed on your system, which is available from most package managers:

```
# on MacOS using Homebrew (https://brew.sh/)
brew install ffmpeg
```

For more information on Whisper please see https://github.com/openai/whisper

The code in this repository is public domain.

## Usage

```
source env/bin/activate
pyenv local 3.11.5
python transcribe_demo.py
```