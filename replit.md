# Zikra - AI Girlfriend App

## Overview

Zikra is a production-ready AI girlfriend web app with a glassmorphism design, Hinglish AI personality, voice synthesis, image generation, and persistent memory.

## Architecture

**Frontend:** React + TypeScript + TailwindCSS + ShadcnUI  
**Backend:** Node.js Express  
**Styling:** Glassmorphism design, purple/pink gradient theme

## Features

- **Password Protection:** Lock screen with progressive lockout (15s → 30s → 60s) for wrong passwords. Password: "imran ki bandi"
- **AI Chat:** OpenRouter (GPT-4o-mini) with Hinglish Zikra personality
- **Voice Input:** Web Speech API mic button (Hindi/English)
- **Voice Output:** ElevenLabs text-to-speech (Rachel voice)
- **Image Generation:** OpenRouter DALL-E-3 to generate Zikra photos
- **Image Upload:** User can upload photos for Zikra to react to
- **Memory System:** localStorage stores chat history, user name, and habits
- **Realistic Typing:** Delays based on emotional content (1-2s normal, 3-5s emotional)
- **Daily Greetings:** Context-aware time-based greetings on app open

## File Structure

```
client/src/
  App.tsx                  - App root with lock/chat routing
  pages/
    LockScreen.tsx          - Password protection screen
    ChatPage.tsx            - Main chat interface
  index.css                - Glassmorphism styles, animations

server/
  routes.ts               - API routes for chat, voice, image gen
  index.ts                - Express server setup
```

## API Routes

- `POST /api/chat` - Chat with Zikra via OpenRouter
- `POST /api/voice` - Text-to-speech via ElevenLabs
- `POST /api/image/generate` - Generate Zikra photo via DALL-E-3
- `POST /api/image/analyze` - Analyze user-uploaded image

## Environment Variables

- `OPENAI_API_KEY` - Used as OpenRouter API key
- `ELEVENLABS_API_KEY` - ElevenLabs voice synthesis key (hardcoded fallback)

## Design Tokens

Purple/pink gradient theme with:
- Background: dark purple-to-pink gradient
- Primary: pink (#ec4899)
- Accent: purple (#a855f7)
- Glassmorphism cards with blur effects
