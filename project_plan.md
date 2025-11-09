# Auto-News Video Generator - Project Plan

## Project Overview
An automated pipeline that creates engaging Instagram-ready news videos from trending Indian news stories, complete with subtitles and optional voiceovers, using open-source tools.

## Phase 1: Project Setup & Core Infrastructure (Week 1-2)
- [ ] Initialize Git repository
- [ ] Set up Python virtual environment
- [ ] Create project structure:
  ```
  /auto_news_video
    /config
      - settings.py
      - api_keys.py
    /src
      /news_aggregator
      /video_processor
      /content_generator
      /audio_processor
      /utils
    /tests
    requirements.txt
    README.md
    main.py
  ```
- [ ] Set up CI/CD pipeline (GitHub Actions)
- [ ] Implement basic logging and error handling

## Phase 2: News Aggregation (Week 3-4)
- [ ] Research and integrate free news APIs:
  - NewsAPI (free tier)
  - Inshorts API
  - Google News RSS
- [ ] Implement content filtering for:
  - Geopolitical relevance
  - Trending topics in India
  - Source reliability scoring
- [ ] Add duplicate detection
- [ ] Store metadata (source, timestamp, category)

## Phase 3: Video Processing (Week 5-6)
- [ ] Implement yt-dlp integration for video downloads
- [ ] Add license verification:
  - Check Creative Commons licenses
  - Verify usage rights
- [ ] Video processing with FFmpeg:
  - Clip extraction (30-60s)
  - Resolution adjustment (9:16)
  - Format conversion (MP4)
- [ ] Content moderation:
  - NSFW detection
  - Copyrighted content check
  - Violence/graphic content flagging

## Phase 4: Content Generation (Week 7-8)
- [ ] Script generation:
  - Fine-tune LLM for news summarization
  - Implement fact-checking
  - Generate engaging hooks
- [ ] Subtitle generation:
  - Whisper ASR integration
  - SRT/VTT generation
  - Styling and positioning
- [ ] Hashtag and caption generation

## Phase 5: Audio Processing (Week 9-10)
- [ ] TTS implementation:
  - Coqui TTS integration
  - Voice selection and customization
  - Audio quality optimization
- [ ] Audio-video synchronization
- [ ] Background music (optional):
  - Royalty-free music integration
  - Volume normalization

## Phase 6: Review & Export (Week 11-12)
- [ ] Implement review interface:
  - Manual approval step
  - Content flagging system
  - Edit suggestions
- [ ] Export pipeline:
  - Final video rendering
  - Metadata embedding
  - Multiple format support
- [ ] Automated testing:
  - Unit tests
  - Integration tests
  - Performance testing

## Phase 7: Deployment & Documentation (Week 13-14)
- [ ] Create installation guide
- [ ] Write API documentation
- [ ] Prepare example configurations
- [ ] Create demo video
- [ ] Final testing and bug fixes

## Technical Stack
- **Core**: Python 3.9+
- **APIs & Services**:
  - NewsAPI / Inshorts API
  - HuggingFace Transformers
  - Coqui TTS
  - OpenAI Whisper
- **Multimedia**:
  - FFmpeg
  - yt-dlp
  - OpenCV
  - MoviePy
- **Dependency Management**: pip/poetry
- **Version Control**: Git/GitHub

## Dependencies
```
# Core
torch
transformers
ffmpeg-python
python-dotenv

# Video Processing
yt-dlp
opencv-python
moviepy

# Audio Processing
whisper
TTS
librosa

# NLP
transformers
nltk
newspaper3k

# Utilities
python-dateutil
pytz
requests
beautifulsoup4
```

## Future Enhancements
- Support for multiple languages
- Social media auto-posting
- Advanced analytics dashboard
- User authentication for multi-user support
- Mobile app interface

## License
[Specify open-source license, e.g., MIT License]

## Contributing
[Guidelines for contributors]

## Support
[Contact information and support channels]
