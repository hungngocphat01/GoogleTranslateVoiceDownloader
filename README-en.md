# GoogleTranslateVoiceDownloader
This small Python script can help you *batch* download Google Translate's voice to your computer from [texttospeech.io](https://texttospeech.io).

**Note:** This guide is targeted to **Vietnamese**. You can simply use [soundoftext](https://soundoftext.com) if you use a different language.

[Phiên bản Tiếng Việt/Vietnamese guide here](README.md)

# Prerequisites
* Python 3 with requests, fake_useragent module installed.

# Installation
* Download or git clone this repository to your computer.

# Usage
* Place a file named *"input.txt"* in the same folder with the script.
* Write your "script" (the conversations you want to download) in that text file. Each line will be downloaded into a seperate *mp3* file.
* Either execute *run.bat* if you're on Windows or *run.sh* if you are on GNU/Linux. You can also run the *.py* file itself but you will not see the program's output (whether the download operation was successful or not).
* Successfully downloaded files will be stored in the *"downloaded"* folder

# Config
* You can also config the script using provided *config.json* file. The file consists of the following keys:
    * `lang`: language code (usually in 2 characters, for example: vi, ja, ko, ... [and a dash and 2 more character to specify the region if the language is spoken in different regions. For example: en-US, en-GB, zh-CN, zh-HK, ...] ) *(Default: vi)*
    * `engine`: the Google Translate engine you would like to use. Just leave it default if you don't know what it is. If the voice sounds weird, or the voice cannot be downloaded, try to change the `engine` to g2, g3, ... *(Default: g1)*
        * Note for `Vietnamese (vi)`: **engine = g1** will download the **old voice** (the funny voice you often see in memes) while **engine = g2** will download the **new voice** (the soft voice used in Google Assistant).
    * `rate`: the speed of the voice *(Default: 0.5)*.
    * `pitch`: the pitch of the voice (high or low) *(Default: 0.5)*.
    * `gender`: the gender of the voice (male, female) *(Default: female)*.
    * `wait`: the interval between downloads in second *(Default: 0.5)*.

## Some examples of `lang` key
| Language name       | `lang` key |
| ------------------- | ---------- |
| Vietnamese          | vi         |
| English (US)        | en-US      |
| English (GB)        | en-GB      |
| English (AU)        | en-AU      |
| Chinese (Simp)      | zh-CN      |
| Chinese (Hong Kong) | zh-HK      |
| Chinese (Taiwan)    | zh-TW      |
| Japanese            | ja         |
| Korean              | ko         |
| Arabic              | ar         |
| Armenian            | hy         |
| Deutsch             | de         |
| Dutch               | nl         |
| Filipino            | fi-PH      |
| Finnish             | fi         |
| French              | fr         |
| French Canadian     | fr-CA      |
| Greek               | el         |
| Hindi               | hi         |

There are much more languages [texttospeech.io](https://texttospeech.io) supports but I can only list a few examples. You can still try the code of your language even it is not listed here (this table just provides some examples). For example: `pt-PT` for Portuguese, `pl` for Polish, `th` for Thai, ...

Audio is provided by [texttospeech.io](https://texttospeech.io). I am not the owner of the API.
My script only re-direct the audio from [texttospeech.io](https://texttospeech.io).


