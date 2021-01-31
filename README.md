# Keats Crawler

This is a python module for downloading videos and resources from KCL's Keats e-learning platform.  

### Requirements
 - Python 3
 - Works on Linux, Windows WSL, macOS

### Installation
1. Clone this repository: `git clone https://github.com/mannmann2/keats_crawler.git`
1. `cd keats_crawler`
1. `pip install -r requirements.txt`
1. [Download chromedriver](https://chromedriver.chromium.org/downloads) for your version of Chrome
1. `sudo apt install ffmpeg` (for Windows you'll need an alternative)

### Usage
1. Self enrol in the Keats module, if not already enrolled
1. Update `config.py` (See below. Cookies must be updated each time your session expires)
1. Run: `python crawl.py`

### Config settings
`MODULE`: Name of module and the folder in which to download files  
`URL`: Keats url for the module  
`PATH`: Location in which to create the module folder  
`PATH_TO_CHROMEDRIVER`: Location of chromedriver executable  
`COOKIES`: Copy and add cookies from your browser after logging into Keats. These can be found by navigating to the Network tab of the browser inspector.  
`DOWNLOAD_RESOURCES`: True/False - Download the non-video resources (ppt, pdf, py, etc)  
`DOWNLOAD_VIDEOS`: True/False - Download videos embedded in Keats (Won't work for videos linked on some other website)  
`VIDEO_PROMPT`: True/False - Prompt before extracting each video for download (Disabling this will automatically download all extracted videos)  
`VIDEO_LIMIT`: Integer or None - Limit the number of videos extracted  
`SKIP_DUPLICATES`: True/False - To skip files already downloaded (Only works if the previous downloads occurred using this package)  
`REMEMBER_DOWNLOADS`: True/False - Add files being downloaded in current crawl to a duplicate filter (Used to check duplicates)  


* Free software: MIT license
