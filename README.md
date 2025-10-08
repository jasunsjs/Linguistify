## Overview
**Linguistify** is an AI-powered dubbing application designed to automate the translation and synchronization of audios of YouTube videos, in different languages. 

This project is inspired by content creators like MrBeast who hire professional voice actors to dub his videos in different languages. Linguistify offers a more versatile and affordable solution for all content creators to reach the world.

## Tech Stack
- **Frontend**: React with Chakra UI
- **Backend**: Python Flask
- **Speech-to-Text (STT)**: [Deepgram](https://deepgram.com/)
- **Text-to-Speech (TTS)**: [ElevenLabs](https://elevenlabs.io/)
- **Translation**: [DeepL](https://www.deepl.com/en/translator)
- **NLP and Translation Refinement**: GPT-4, Hugging Face

## Workflow
1. **Speech-to-Text**
   - Transcribes separated audio with Deepgram
   - Tracks timestamps of each utterance
3. **Translation**
   - Translates entire text into selected language using **DeepL**
5. **Processing & Refinement**
   - Breaks down translated text into individual utterances
   - Rephrases translated utterances using GPT-4 (with before & after context) for clarity and conciseness to match original utterance durations
6. **Audio Generation**  
   - Generates speech using Elevenlabs, incorporating in pauses between utterances
   - Slightly adjusts individual utterance speed if necessary, fully matching original durations
7. **Attach to Original Video**  
   - New audio is attached into the original video for final output
