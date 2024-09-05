# Amazon Rekognition

- Computer vision on-demand
- Its main purpose is object and scene detection (can be used for face detection on our own collection of images)
- We can do facial analysis and facial search to do user verification, people counting
- We can create a database of "familiar faces" or compare against celebrities
- Use cases:
    - Image moderation
    - Facial analysis
    - Celebrity recognition
    - Face comparison
    - Text in image
    - Video analysis. Examples:
        - Object/people/celebrities marked on a timeline
        - People pathing
- Input images can come from S3 or provided as bytes as part of the request
- Facial recognition depends on good lightning, angle, visibility of eyes, resolution
- Video must come from Kinesis Video Streams. It must be:
    - H.264 encoded
    - 5-30 FPS
    - Favor resolution over framerate
- We can use it with Lambda to trigger image analysis upon upload

## Recognition Custom Labels

- We can train the service with a small set of labeled images
- We can use our own labels for unique items
- Example: NFL uses custom labels to identify team logos, pylons and foam fingers in images

## Content Moderation

- Rekognition can automatically detect inappropriate, unwanted or offensive content
- Examples: filter out harmful images in social media, broadcast media and advertising
- Integrates with Amazon Augmented AI (Amazon A2I) for human review
- Custom Moderation Adaptor:
    - Extends Rekognition capabilities by providing our own labeled set of images
    - We can enhance the accuracy of Content Moderation or create a specific use case of moderation