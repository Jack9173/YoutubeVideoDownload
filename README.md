# YoutubeVideoDownload

This Python code creates a simple graphical user interface (GUI) using the tkinter library to download videos from YouTube. Here's a breakdown:

Imports:

from tkinter import *: Imports all widgets from the tkinter library.
from pytube import YouTube: Imports the YouTube class from the pytube library for downloading videos.
Main Window Setup:

root = Tk(): Creates the main application window.
root.geometry('700x300'): Sets the window size to 700x300 pixels.
root.resizable(0, 0): Disables resizing of the window.
root.title("YouTube Video Downloader"): Sets the title of the window.
Instructions Label:

Label(root, ...).pack(): Creates a label to display instructions to the user.
Link Entry:

link = StringVar(): Creates a variable to store the entered URL.
Label(root, ...).place(...): Creates a label prompting the user to paste the link.
Entry(root, ...).place(...): Creates an entry widget for the user to paste the YouTube video link.
Download Function:

def Downloader():: Defines the function to handle downloading a video.
url = YouTube(str(link.get())): Creates a YouTube object using the URL from the entry.
video = url.streams.first(): Gets the first available video stream.
video.download(): Downloads the video.
Label(root, ...).place(...): Creates a label to display a "DOWNLOADED" message upon success.
Download Button:

Button(root, ...).place(...): Creates a button with clear text and styling to trigger the download function.
Main Loop:

root.mainloop(): Starts the main event loop of the Tkinter application, waiting for user interactions.
Important Note:

Downloading copyrighted content without permission is illegal. Use this code responsibly and ethically.
README Content for GitHub:

Features:

User-friendly GUI for easy interaction.
Basic Download Functionality.
Installation:

Prerequisites: Ensure you have Python 3 (https://www.python.org/downloads/) and pip (package manager) installed.

Install Libraries: Open a terminal/command prompt and run:

Bash
pip install tkinter pytube
Use code with caution.

Usage:

Clone or download the repository.

Run the script from your terminal:

Bash
python youtube_downloader.py  # Replace with the actual filename
