# Amazon Polly

- Neural Text-to-Speech engine, provides many voices and languages
- Accepts lexicons: we can customize pronunciations of specific words and phrases
- Supports SSML format:
    - SSML - Speech Synthesis Markup Language
    - Markup for our text to indicate how to pronounce it
    - Gives control over emphasis, pronunciations, breathing, whispering, speech rate, pitch, pauses
    - Example: `<speak>`Hello, `<break />` how are yoy?`</speak>`
- Supports Speech Marks:
    - Can encode when sentence/word starts and ends in the audio stream
    - Useful for lip-synching animation