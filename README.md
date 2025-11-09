# OpenRouter Multi-Model Chat

A powerful, single-file web application for chatting with multiple AI models simultaneously through OpenRouter's unified API.

## 🚀 Live Demo

**[Launch App](https://mbbrinkman.github.io/my_api_chat/api-chat.html)**

## ✨ Features

### Multi-Model Conversations
- **Parallel Mode**: All selected models respond independently to your messages
- **Serial Mode**: Models respond one after another, each seeing previous responses
- **Rotating Mode**: Like serial, but model order rotates each turn
- **Autonomous Mode**: Models converse with each other without human input

### OpenRouter Integration
- Access 100+ AI models from multiple providers through a single API
- Support for models from:
  - Anthropic (Claude)
  - OpenAI (GPT-4, GPT-3.5)
  - Google (Gemini)
  - Meta (Llama)
  - Mistral, Cohere, and many more

### Advanced Features
- **Vision Support**: Attach images to messages (model-dependent)
- **Message Editing**: Edit and regenerate any message in the conversation
- **Conversation Branching**: Edit past messages to explore different conversation paths
- **System Prompts**: Set custom system prompts per model or globally
- **Real-time Streaming**: See responses as they're generated
- **Typing Indicator**: Visual feedback during message processing

### Customization
- **Full Parameter Control**: Configure temperature, top_p, max_tokens, and all OpenRouter parameters
- **API Key Management**: Securely store multiple API keys
- **Model Presets**: Save and reuse model configurations
- **Prompt Library**: Create and manage reusable system prompts

### Data Management
- **Local Storage**: All data saved in your browser
- **Export/Import**: Backup and restore your models, keys, and conversations
- **Conversation History**: Automatic saving with clear all option

### User Experience
- **Single-File App**: No installation, just open in browser
- **Dark Theme**: Easy on the eyes
- **Markdown Support**: Rendered responses with LaTeX math support
- **Mobile Friendly**: Works on iPhone and all modern browsers
- **Keyboard Shortcuts**: Send messages with Enter

## 🎯 Use Cases

- **Model Comparison**: Compare responses from different models side-by-side
- **AI Debates**: Watch models discuss and build on each other's ideas
- **Multi-Perspective Analysis**: Get diverse viewpoints on complex questions
- **Cost Optimization**: Use cheaper models for simple tasks, powerful ones for complex
- **Experimentation**: Test different model configurations and parameters

## 🚀 Quick Start

1. **Open the app**: [Click here](https://mbbrinkman.github.io/my_api_chat/api-chat.html)

2. **Get an API key**: Visit [openrouter.ai/keys](https://openrouter.ai/keys) and create a free account

3. **Add your API key**:
   - Go to Settings tab
   - Click "Add OpenRouter API Key"
   - Paste your key and give it a name

4. **Add a model**:
   - Scroll to "Add New Model" section
   - Give it a name (e.g., "Claude")
   - The template auto-populates with your API key
   - Change `model_id` to your desired model (e.g., `anthropic/claude-3.5-sonnet`)
   - Click "Add Model"

5. **Start chatting**:
   - Go to Chat tab
   - Click "Select Models" and check your model
   - Type your message and hit Send!

## 📋 Available Models

Browse all available models at [openrouter.ai/models](https://openrouter.ai/models)

Popular choices:
- `anthropic/claude-3.5-sonnet` - Claude 3.5 Sonnet
- `openai/gpt-4-turbo` - GPT-4 Turbo
- `google/gemini-pro-1.5` - Google Gemini Pro
- `meta-llama/llama-3.1-70b-instruct` - Llama 3.1 70B
- `mistralai/mistral-large` - Mistral Large

## 🔧 Configuration

### Model Parameters

Customize model behavior with these parameters:

- `temperature` (0.0-2.0): Controls randomness/creativity
- `max_tokens`: Maximum response length
- `top_p`: Nucleus sampling threshold
- `top_k`: Limit sampling to top K tokens
- `frequency_penalty`: Reduce word repetition
- `presence_penalty`: Encourage topic diversity
- `repetition_penalty`: Alternative repetition control
- `seed`: For deterministic outputs
- `provider`: Force specific provider
- `transforms`: Content filtering options

### Multi-Model Modes

**Parallel**: Best for comparing different models' approaches to the same question.

**Serial**: Great for building on ideas, where each model adds to the conversation.

**Rotating**: Ensures fair turn-taking in model conversations.

**Autonomous**: Let models have extended discussions without interruption.

## 💾 Data & Privacy

- All data stored locally in your browser
- No server-side processing
- API keys stored in browser localStorage
- Export your data anytime for backup
- Clear history to remove all stored data

## 🛠️ Technical Details

- **Single HTML file**: Entire app in one file (~2000 lines)
- **No dependencies**: Pure JavaScript, no frameworks
- **Markdown rendering**: Built-in markdown and LaTeX support
- **Streaming API**: Real-time response rendering
- **Error handling**: User-friendly error messages
- **Mobile optimized**: Responsive design for all devices

## 📖 Documentation

### OpenRouter Documentation
- [OpenRouter Docs](https://openrouter.ai/docs)
- [API Reference](https://openrouter.ai/docs/api-reference)
- [Supported Models](https://openrouter.ai/models)

### Tips

1. **Save your configuration**: Use Export Data to backup your models and keys
2. **Test models**: Start with parallel mode to compare different models
3. **Use system prompts**: Give models specific roles or instructions
4. **Manage costs**: Check model pricing at openrouter.ai before use
5. **Temperature settings**: Lower (0.3-0.7) for factual, higher (0.8-1.5) for creative

## 🤝 Contributing

This is an open-source project. Feel free to:
- Report issues
- Suggest features
- Submit pull requests
- Share your model configurations

## 📄 License

MIT License - feel free to use, modify, and distribute.

## 🙏 Credits

Built with:
- [OpenRouter](https://openrouter.ai) - Unified AI model API
- [KaTeX](https://katex.org) - Math rendering
- [marked](https://marked.js.org) - Markdown parsing

---

**[Start Chatting Now →](https://mbbrinkman.github.io/my_api_chat/api-chat.html)**
