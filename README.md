# Seamless-Large-File-Downloads-to-Google-Drive
A Python script to automate downloading large files directly to Google Drive using Google Colab. The script checks for available storage, determines file size, and provides a progress report with download speed for efficient file management.

# Google Drive File Downloader with Storage Check

This Python script automates the process of downloading files directly to Google Drive via Google Colab. It ensures efficient file management by verifying storage availability, handling large files, and providing detailed progress tracking during downloads.

## Features
- **Google Drive Integration**: Automatically mounts Google Drive and saves files in a dedicated folder (`GCdownload`).
- **Storage Management**: Checks available Google Drive storage before initiating the download.
- **File Size Detection**: Automatically retrieves and displays the file size.
- **Smart File Naming**: Handles long or complex file names by hashing them if necessary.
- **Download Progress**: Displays real-time progress, download speed, and percentage completed.

## Prerequisites
- A Google account with access to Google Drive.
- Python installed in Google Colab.

## Installation
1. Open Google Colab: [Google Colab](https://colab.research.google.com/).
2. Copy and paste the script into a new Colab notebook.
3. Run the cells to execute the script.

## Usage
1. Run the script in Google Colab.
2. Enter the download link when prompted.
3. The script will:
   - Mount your Google Drive.
   - Check for sufficient storage.
   - Download the file into a `GCdownload` folder within your Google Drive.

## Code Overview
```python
from google.colab import drive
import requests
import os
import shutil
import time
import sys
import hashlib

# Main Steps:
# 1. Mount Google Drive.
# 2. Get the file download link and determine its name.
# 3. Verify available Google Drive storage and file size.
# 4. Download the file in chunks and track progress.

# Function Definitions:
# - mount_drive(): Mounts Google Drive in the Colab environment.
# - get_download_details(): Retrieves the file download link and determines its name.
# - check_storage_and_file_size(): Ensures sufficient space for the download.
# - download_file(): Downloads the file while displaying progress and speed.
