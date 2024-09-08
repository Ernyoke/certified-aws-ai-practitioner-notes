# Amazon Transcribe

- It transcribes speech to text
- Uses a deep learning process called automatic speech recognition (ASR) to convert speech to text quickly and accurately
- It can automatically remove any PII data using Redaction
- Speech input can be in FLAC, MP3, MP4 or WAV formats in a specified language
- Supports streaming audio (HTTP/2, WebSockets) for French, English and Spanish
- Can identify and distinct speakers
- Can do channel identification:
    - Example: two callers could be transcribed separately
- Can automatically detect language (it can detect the dominant one spoken)

## Improving Accuracy

- Custom vocabulary (for words):
    - Vocabulary Lists: just a list a special words
    - Vocabulary Tables: can include `SoundsLike`, `IPA` and `DisplayAs`
    - Can be used for technical words, acronyms, jargon, etc.
- Custom Language Models (for context):
    - We can train Transcribe model on our own domain-specific text data
    - Can learn the context associated with a given word
- We can use both for highest transcription accuracy

## Amazon Transcribe Medical

- Automatically converts medical-related speech to text (HIPAA compliant)
- Has the ability to transcribe medical terminologies such as:
    - Medicine names
    - Procedures
    - Conditions and diseases
- Supports both real-time (microphone) and batch (upload multiple files) transcriptions

## Use Cases

- Call Analytics:
    - Trained specifically for customer service and sales calls
    - Real-time transcriptions and insights
    - Sentiment, talk speed, interruptions, look for specific phrases
- Medical:
    - Trained on medical terminology
    - HIPAA-eligible
- Subtitling:
    - Live subtitle output