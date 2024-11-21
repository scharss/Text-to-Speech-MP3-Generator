# Text-to-Speech MP3 Generator

**This project converts the content of a text file (`article.txt`) into an MP3 audio file using the `edge-tts` library.**  
It is configured to use a male voice in Latin American Spanish (`es-MX-JorgeNeural`), but you can customize the voice and language according to your preferences.

---

## Features

- Converts text into MP3 format audio.
- Compatible with both Google Colab and local environments.
- Uses natural voices powered by Microsoft Azure Text-to-Speech.

---

## Requirements

- **Python 3.7 or higher**
- Required libraries:
  - [`edge-tts`](https://github.com/rany2/edge-tts): For text-to-speech conversion.
  - [`nest_asyncio`](https://github.com/erdewit/nest_asyncio): Enables asynchronous functions in Google Colab.

---

## Installation

### On Your Local Machine

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/text-to-speech-mp3-generator.git
   cd text-to-speech-mp3-generator
## Install the required libraries:
pip install edge-tts nest_asyncio

Place your text file named article.txt in the root directory of the project.

Run the main script:
```bash
python main.py
```
The audio file article_audio.mp3 will be generated in the same directory.

On Google Colab
Open Google Colab and upload the project files (main.py and article.txt).

Install the required libraries:
```bash
!pip install edge-tts nest_asyncio
```
Execute the provided code for Colab.

Once the script finishes, download the generated file article_audio.mp3 from Colab.

Configuration
You can customize the language and voice by modifying the voice parameter in the script:

```bash
voice = "es-MX-JorgeNeural"  # Male Latin American Spanish voice
```

Available Voices
Some examples include:

es-MX-JorgeNeural (male, Mexican Spanish)
es-MX-DaliaNeural (female, Mexican Spanish)
es-US-AlonsoNeural (male, US Spanish)

Troubleshooting
Error: RuntimeError: This event loop is already running
This error occurs in Google Colab. It is resolved by using the nest_asyncio library, which is included in the script:

```bash
import nest_asyncio
nest_asyncio.apply()
```

Error: FileNotFoundError: article.txt
Ensure the article.txt file exists in the working directory. You can check the files in your current directory with:

ls


