# TikTok Video Generator

This script generates TikTok videos using trending topics from a specified region. It creates a video with custom subtitles and text-to-speech (TTS) audio, allowing you to customize various aspects like the length, voice tone, and more.

## Demo

[![Demo](http://img.youtube.com/vi/5Y4JmIlwCkw/0.jpg)](http://www.youtube.com/watch?v=5Y4JmIlwCkw "Demo Video")


## Features

- Fetches trending topics from a specified region or the default (`united_states`).
- Generates a video script using AI, tailored to your preferences.
- Downloads related images to create a visually engaging video.
- Converts the script to audio using TTS and adds subtitles.
- Outputs the final video with all elements combined.
- Option to automatically upload the video after creation.

## Usage

Run the script with the following command-line arguments:

```bash
python your_script.py [options]
```

## Options

- `--topic`: The topic for the video. If not provided, a trending topic will be selected.
- `--length`: The length of the video (e.g., 10 sec). Default is 10 sec.
- `--voice_tone`: The voice tone for the video script (e.g., Content Creator). Default is Content Creator.
- `--additionals`: Additional JSON keys to include (e.g., video_script, video_title, video_hashtags). Default is
  ```python
  ['video_script', 'video_title', 'video_hashtags']
  ```
- `--output`: The output file path for the generated video. Default is final_video.mp4.
- `--upload`: Flag to upload the video after creation.
- `--region`: The region to fetch trending topics from (e.g., france). Default is united_states.
- `--regions`: Display the list of available regions.

## Examples

1. Fetch a trending topic from France and create a video:
    ```bash
    python auto.py --region france --length "20 sec" --voice_tone "Informative" --output "french_trend.mp4" --upload
    ```

2. List all available regions:
   ```bash
   python auto.py --regions
   ```
   
4. Generate a video with a specific topic and upload it:
   ```bash
    python auto.py --topic "COVID-19 updates" --length "15 sec" --voice_tone "Serious" --output "covid_update.mp4" --upload
   ```
5. Generate a video with a trending topic from the default region:
   ```bash
   python auto.py --length "10 sec" --voice_tone "Content Creator" --upload
   ```

This script is designed to automate the creation of TikTok videos, making it easier to stay on top of trends and generate content quickly.
