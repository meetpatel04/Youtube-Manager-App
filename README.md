# YouTube Manager App

## Overview
The YouTube Manager app is a Python-based command-line application designed to manage and organize your list of YouTube videos. It allows users to:

- List all stored videos.
- Add new videos.
- Update existing video details.
- Delete videos.

The app reads and writes video data to a JSON-formatted file (`youtube.txt`).

---

## Features

### 1. List All Videos
Displays all videos currently stored in the `youtube.txt` file, showing their names and durations.

### 2. Add a Video
Prompts the user to enter the name and duration of a video and appends it to the existing list.

### 3. Update a Video
Allows users to modify the name and duration of an existing video by selecting it from the list.

### 4. Delete a Video
Enables users to remove a video from the list by selecting its index.

---

## Installation

### Prerequisites
- Python 3.9 or above.

### Steps
1. Clone or download the project.
2. Ensure `youtube.txt` exists in the same directory as the script, with initial data structured like this:
   ```json
   [
       {"name": "SQL", "time": "2 Hours"},
       {"name": "Python", "time": "5 Hrs"}
   ]
   ```
   If the file does not exist, the app will create it during execution.
3. Run the script using:
   ```bash
   python youtube_manager.py
   ```

---

## Usage
1. Launch the app.
2. Follow the menu options displayed:
   - `1`: List all videos.
   - `2`: Add a new video.
   - `3`: Update an existing video.
   - `4`: Delete a video.
   - `5`: Exit the app.
3. Enter your choice and follow the prompts.

---

## Code Structure

### `youtube_manager.py`
- **Functions**:
  - `load_data`: Reads and parses video data from `youtube.txt`.
  - `save_data_helper`: Writes video data back to `youtube.txt`.
  - `list_all_videos`: Displays all videos with their details.
  - `add_video`: Adds a new video to the list.
  - `update_video`: Updates video details by index.
  - `delete_video`: Deletes a video by index.
- **Main Functionality**:
  - Displays a menu and handles user input to invoke the corresponding functionality.

### `youtube.txt`
- Stores video data in JSON format.

---

## Example
### Sample `youtube.txt` File:
```json
[
    {"name": "SQL", "time": "2 Hours"},
    {"name": "Python", "time": "5 Hrs"}
]
```

### Sample Interaction:
```text
 YouTube Manager | Choose an option
 1. List all YouTube videos
 2. Add a YouTube video
 3. Update a YouTube video's details
 4. Delete a YouTube video
 5. Exit the app

Enter your choice: 1

**********************************************************************
1. SQL, Duration: 2 Hours
2. Python, Duration: 5 Hrs
**********************************************************************
```

---

## Future Enhancements
- Add a search functionality to find videos by name.
- Integrate a graphical user interface (GUI).
- Enable support for additional video attributes like URL and description.

---

