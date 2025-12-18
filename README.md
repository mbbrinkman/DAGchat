# OpenRouter Multi-Model Chat

A single-file web application for chatting with multiple AI models simultaneously through OpenRouter's unified API.

## Live Demo

https://mbbrinkman.github.io/my_api_chat/api-chat.html

## Features

### Multi-Model Conversation Modes
- **Parallel**: All selected models respond independently to each message
- **Serial**: Models respond sequentially, each seeing previous model responses
- **Rotating**: Serial mode with model order rotation on each turn
- **Autonomous**: Models converse with each other without user input

### Core Functionality
- Real-time streaming responses
- Message and response editing
- Conversation branching (edit past messages to explore alternatives)
- Image attachments for sending to vision models
- Image generation support (receive images from image generation models)
- Model browser (fetch, search, and sort all available OpenRouter models)
- Configurable system prompts (per-model or global override)
- IndexedDB storage for unlimited conversations with images (50 MB to several GB)
- Export/import functionality for data backup
- Mobile-friendly with reliable image support on iPhone/iPad

### Model Configuration
- Full access to OpenRouter API parameters including temperature, top_p, max_tokens, frequency/presence penalties, and provider-specific options
- Saved model presets for reuse
- Multiple API key management
- Reusable system prompt library

## Setup

1. Open the application at https://mbbrinkman.github.io/my_api_chat/api-chat.html
2. Create an OpenRouter account and obtain an API key at https://openrouter.ai/keys
3. In Settings, add your API key
4. Browse available models using the model browser, or manually add a model configuration
5. Select your model(s) and start chatting

### Using the Model Browser

1. Go to Settings tab
2. Scroll to "Browse OpenRouter Models"
3. Click "Load Models" to fetch the live catalog
4. Search by name, ID, or description
5. Sort by date (newest first), name, or context length
6. Click any model to auto-populate the Add New Model form
7. Edit configuration if needed and click "Add Model"

The browser displays context length, pricing per million tokens, and release date for each model.

## OpenRouter Integration

This application uses OpenRouter as the sole API provider, which provides unified access to models from multiple providers including Anthropic, OpenAI, Google, Meta, Mistral, and others. See https://openrouter.ai/models for the complete model catalog.

Example model IDs:
- anthropic/claude-3.5-sonnet
- openai/gpt-4-turbo
- google/gemini-pro-1.5
- meta-llama/llama-3.1-70b-instruct

## Technical Details

- Single HTML file application (~2800 lines)
- No build process or dependencies required
- Client-side JavaScript only
- Uses KaTeX (via CDN) for LaTeX math rendering
- Custom markdown rendering for bold, italic, code blocks
- IndexedDB for data persistence (50 MB to several GB storage)
- Supports all modern browsers including mobile (iPhone/iPad tested)

## Privacy

All data is stored locally in your browser using IndexedDB. No information is sent to any server except OpenRouter API calls for model responses. API keys, conversations, and all settings remain private on your device.

## Image Generation

The application supports receiving images from image generation models on OpenRouter:

1. Add a model with "image" in its output modalities (filter by output modality on openrouter.ai/models)
2. Request image generation in your message (e.g., "generate an image of a sunset")
3. Generated images appear automatically in the conversation
4. Multiple images per response are supported
5. Images are displayed inline with full-width responsive sizing

Images are returned as base64-encoded data URLs and stored in the conversation history.

## Configuration Parameters

The application supports all OpenRouter API parameters:

- temperature: Response randomness (0.0-2.0)
- max_tokens: Maximum response length
- top_p: Nucleus sampling threshold
- top_k: Token sampling limit
- frequency_penalty: Penalize repeated tokens (-2.0 to 2.0)
- presence_penalty: Penalize topic repetition (-2.0 to 2.0)
- repetition_penalty: Alternative repetition control
- min_p: Minimum probability threshold
- top_a: Adaptive sampling
- seed: Deterministic output
- logit_bias: Token probability adjustment
- response_format: Structured output control
- provider: Force specific provider
- transforms: Content filtering
- reasoning: Enable extended thinking/reasoning

See OpenRouter documentation for parameter details: https://openrouter.ai/docs

## License

CC0 1.0 Universal - Public Domain Dedication

This work is released into the public domain. You can copy, modify, distribute and perform the work, even for commercial purposes, without asking permission.

## Credits

- OpenRouter API: https://openrouter.ai
- KaTeX: https://katex.org

