# YouTube Video Bookmark Chrome Extension

This Chrome extension allows users to create bookmarks for specific timestamps in YouTube videos. It provides a convenient way to mark important moments in videos for later reference.

## Features

- Automatically detects YouTube video pages and injects bookmarking functionality.
- Allows users to add bookmarks at specific timestamps in videos.
- Displays existing bookmarks for the current video.
- Supports playback of bookmarks by clicking on them.
- Allows users to delete bookmarks they no longer need.

## Installation

To install the extension, follow these steps:

1. Download or clone the repository to your local machine.
2. Open Google Chrome and go to `chrome://extensions`.
3. Enable Developer mode in the top right corner.
4. Click on the "Load unpacked" button and select the directory where you cloned or downloaded the repository.
5. The extension should now be installed and ready to use.

## Usage

1. Navigate to a YouTube video page in Google Chrome.
2. The extension automatically detects the video and adds a bookmark button to the video player controls.
3. Click on the bookmark button at the desired timestamp to add a bookmark.
4. Existing bookmarks for the video will be displayed below the video player.
5. Click on a bookmark to play the video from the corresponding timestamp.
6. To delete a bookmark, click on the delete button next to the bookmark.

## Technologies Used

- JavaScript
- Chrome Extension APIs
- HTML
- CSS

## Files Overview
# background.js:

This file contains the background script for the Chrome extension.
It listens for updates to browser tabs and detects when a tab navigates to a YouTube video page.
Upon detecting a YouTube video page, it sends a message to the content script to initialize the bookmarking functionality.

# contentScript.js:

The content script injected into YouTube video pages.
Responsible for adding a bookmark button to the YouTube video player controls.
Handles bookmarking events such as adding new bookmarks and retrieving existing bookmarks from Chrome storage.
Communicates with the background script and popup script using message passing.

# popup.js:

Manages the behavior of the popup window that appears when the extension icon is clicked.
Handles user interactions within the popup, such as playing bookmarks and deleting bookmarks.
Communicates with the content script and background script to perform bookmark-related actions.

# utils.js:

Contains utility functions used across different parts of the extension.
Provides a function to retrieve the URL of the currently active tab.

# assets/bookmark.png:

Image asset used for the bookmark button displayed on the YouTube video player controls.

# manifest.json:

Configuration file that provides metadata about the extension.
Specifies the background scripts, content scripts, permissions, and other details required by the extension.
Defines the extension's name, version, description, icons, and other properties.

## Additional Information:
# Chrome Extension APIs:

The project utilizes various Chrome Extension APIs, such as chrome.tabs, chrome.storage, and chrome.runtime, to interact with the browser environment.
These APIs enable communication between different components of the extension and provide access to browser functionality.