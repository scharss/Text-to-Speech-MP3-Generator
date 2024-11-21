Text-to-Speech MP3 Generator
This project converts the content of a text file (article.txt) into an MP3 audio file using the edge-tts library. It is configured to use a male voice in Latin American Spanish (es-MX-JorgeNeural), but you can customize the voice and language to fit your needs.

Features
Converts text into audio in MP3 format.
Compatible with both Google Colab and local environments.
Uses natural voices from Microsoft Azure Text-to-Speech.
Requirements
Python 3.7 or higher.
Required libraries:
edge-tts: For text-to-speech conversion.
nest_asyncio: Enables asynchronous functions in Google Colab.
Installation
On Your Local Machine
Clone this repository:

bash
Copiar código
git clone https://github.com/your-username/text-to-speech-mp3-generator.git
cd text-to-speech-mp3-generator
Install the required libraries:

bash
Copiar código
pip install edge-tts nest_asyncio
Place your text file named article.txt in the root directory of the project.

Run the main script:

bash
Copiar código
python main.py
The audio file article_audio.mp3 will be generated in the same directory.

On Google Colab
Open Google Colab and upload the project files (main.py and article.txt).

Install the required libraries:

python
Copiar código
!pip install edge-tts nest_asyncio
Execute the adjusted code for Colab in the provided notebook (main.ipynb).

Download the generated article_audio.mp3 file from the environment.

Configuration
You can customize the language and voice by modifying the voice parameter in the Python script:

python
Copiar código
voice = "es-MX-JorgeNeural"  # Male Latin American Spanish voice
Available options include:

es-MX-JorgeNeural (male, Mexican Spanish)
es-MX-DaliaNeural (female, Mexican Spanish)
es-US-AlonsoNeural (male, US Spanish)
For a complete list of supported voices, visit the Microsoft Azure Voices Documentation.

Common Issues
Error: RuntimeError: This event loop is already running
This error occurs in Google Colab. It is resolved by using the nest_asyncio library, which is already included in the code.

Error: FileNotFoundError: article.txt
Ensure the article.txt file is in the working directory. You can check with:

python
Copiar código
!ls
License
This project is licensed under the MIT License. You are free to use, modify, and distribute this code.

If you have any questions or encounter an issue, feel free to open an issue in this repository! 😊

This README.md provides clear instructions for users to install, configure, and run the project, as well as troubleshoot common problems. Let me know if you want to add more details or make adjustments!
