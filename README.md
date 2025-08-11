# YouTube to Bilibili Upload Tool v2.2

Automated tool for downloading YouTube videos with Chinese subtitles and uploading to Bilibili.

## Features

### v2.2 - AI Translation Update
- 🤖 **AI-Powered Translation**: High-quality subtitle translation using multiple AI services
- 🆓 **Free Gemini Support**: Use Google's Gemini API for free high-quality translation
- 💎 **Premium Services**: Support for OpenAI GPT and DeepL for best quality
- 🎯 **Smart Subtitles**: Automatically burns Chinese subtitles into videos
- 🖼️ **Custom Covers**: Upload custom cover images for Bilibili
- 🗑️ **Video Management**: Delete videos from library
- 🌐 **Web Interface**: Easy-to-use browser interface

## Translation Options

1. **Auto Chinese Subtitles (Fast)**: Uses YouTube's auto-generated Chinese subtitles
2. **AI Translation - Gemini (Free)**: High-quality translation using Google Gemini
3. **AI Translation - OpenAI GPT**: Professional translation using GPT-3.5/4
4. **AI Translation - DeepL**: Best quality translation service

## Installation

1. Clone the repository:
```bash
git clone https://github.com/bijdolphin/youtube-bilibili-upload.git
cd youtube-bilibili-upload
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Download FFmpeg (required for subtitle burning):
```bash
# macOS
brew install ffmpeg

# Or download from https://ffmpeg.org/download.html
```

## Configuration

### Bilibili Credentials
Edit `clean_app_v22.py` and update your Bilibili credentials:
```python
SESSDATA = "your_sessdata"
BILI_JCT = "your_bili_jct"
BUVID3 = "your_buvid3"
```

### AI Translation API Keys (Optional)
For premium translation services, set environment variables:
```bash
export OPENAI_API_KEY="your_openai_key"
export DEEPL_API_KEY="your_deepl_key"
export GEMINI_API_KEY="your_gemini_key"  # Get free key from https://makersuite.google.com/app/apikey
```

## Usage

1. Start the application:
```bash
python clean_app_v22.py
```

2. Open your browser and navigate to:
```
http://localhost:3000
```

3. Follow the three-step process:
   - **Step 1**: Enter YouTube URL and select translation mode
   - **Step 2**: Upload custom cover (optional)
   - **Step 3**: Select video and upload to Bilibili

## File Structure

```
├── clean_app_v22.py          # Main application (latest version)
├── subtitle_helper.py        # Auto subtitle download helper
├── ai_subtitle_translator.py # AI-powered translation module
├── requirements.txt          # Python dependencies
├── videos/                   # Downloaded videos directory
├── covers/                   # Custom covers directory
└── README.md                # This file
```

## Requirements

- Python 3.7+
- FFmpeg
- yt-dlp
- Flask
- bilibili-api-python

## Troubleshooting

### No Chinese Subtitles
- YouTube doesn't generate native Chinese captions for English videos
- Use AI translation mode for better quality
- Gemini mode is free and provides good results

### Connection Issues
- Try using VPN or proxy
- Use mobile hotspot if on restricted networks
- Check firewall settings

### Translation Quality
- AI translation (especially DeepL) provides much better quality than auto-generated
- Gemini is free and works well for most content
- For professional content, consider DeepL or GPT-4

## Version History

- **v2.2**: Added AI-powered translation with multiple services
- **v2.1**: Added delete videos and custom cover upload
- **v2.0**: Web interface with subtitle support
- **v1.0**: Basic download and upload functionality

## License

MIT License

## Contributing

Pull requests are welcome! For major changes, please open an issue first.

## Support

For issues and questions, please open an issue on GitHub.