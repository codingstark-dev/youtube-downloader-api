## YouTube Downloader API

This API built using Flask allows users to retrieve video information from YouTube and download videos in specified resolutions or audio format.

### API Endpoints

#### Fetch Video Information

- **Endpoint**: `/api/video_info`
- **Method**: `GET`
- **Parameters**:
  - `url` (required): The YouTube video URL
- **Response**:
  - JSON containing video title, available resolutions with download links, audio information, and thumbnail URL.

#### Download Video/Audio

- **Endpoint**: `/api/download`
- **Method**: `GET`
- **Parameters**:
  - `url` (required): The YouTube video URL
  - `resolution` (required): Video resolution (use 'audio' for audio-only)
- **Response**:
  - Downloads the requested video or audio file.

### Setup Instructions

1. Install Python.
2. Install dependencies:
    ```
    pip install flask flask-cors pytube
    ```
3. Run the application:
    ```
    python app.py
    ```
4. Access the API endpoints using `http://localhost:5000`.

### Usage

#### Fetch Video Information

```bash
GET /api/video_info?url=<YouTube_video_URL>
