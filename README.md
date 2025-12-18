# DAGchat

A single-file web application for orchestrating multi-model AI conversations using a visual DAG (Directed Acyclic Graph) interface. Build complex workflows where models can debate, critique, synthesize, and collaborate.

**[Try the Live Demo](https://mbbrinkman.github.io/DAGchat/DAGchat.html)**

## Features

### Visual DAG Editor
- **Drag-and-drop node creation** - Add model nodes and position them visually
- **Edge drawing** - Connect nodes by dragging from output to input ports
- **Cycle detection** - Prevents invalid circular dependencies
- **Templates** - Pre-built patterns: Chain, Parallel, Diamond, Debate, Critic Loop, Ensemble

### Multi-Model Orchestration
- **Sequential processing** - Chain models where each sees the previous output
- **Parallel execution** - Multiple models process the same input simultaneously
- **Merging outputs** - Combine results from multiple upstream models
- **Context modes** - Control what each node sees (inputs only, inputs + user message, full history)

### Workflow Patterns

| Template | Description |
|----------|-------------|
| **Single** | Basic single-model chat |
| **Chain** | A → B → C sequential processing |
| **Parallel** | Multiple models respond independently |
| **Diamond** | Split → parallel paths → merge |
| **Debate** | Two models argue, third judges |
| **Critic Loop** | Draft → Critique → Refine |
| **Ensemble** | Three models + synthesizer |

### Node Configuration
- **Model selection** - Assign any configured model to each node
- **System prompts** - Per-node or inherited from DAG-level settings
- **Context mode** - inputs-only, inputs-plus-user, or full-history
- **Reasoning stripping** - Remove chain-of-thought from forwarded output
- **Terminal node** - Designate which node's output goes to the user

### Core Features
- Real-time streaming responses
- Message editing and regeneration
- Conversation history with search
- File attachments (images, PDFs, text files)
- Extended thinking/reasoning support
- LaTeX math rendering (KaTeX)
- Markdown formatting

### Keyboard Shortcuts
| Shortcut | Action |
|----------|--------|
| `Ctrl+Z` | Undo DAG operation |
| `Ctrl+Y` / `Ctrl+Shift+Z` | Redo |
| `Ctrl+C` | Copy selected node |
| `Ctrl+V` | Paste node |
| `Delete` / `Backspace` | Delete selected node |
| `Escape` | Deselect / close panels |

## Setup

1. Download `DAGchat.html`
2. Open in any modern browser
3. Go to Settings tab
4. Add your OpenRouter API key
5. Browse and add models
6. Switch to DAG tab and build your workflow
7. Start chatting!

## OpenRouter Integration

DAGchat uses [OpenRouter](https://openrouter.ai) for unified access to models from Anthropic, OpenAI, Google, Meta, Mistral, and more.

Example models:
- `anthropic/claude-sonnet-4-20250514`
- `openai/gpt-4o`
- `google/gemini-2.0-flash-exp`
- `meta-llama/llama-3.3-70b-instruct`

## Technical Details

- **Single HTML file** (~4000 lines, ~115KB)
- **No build process** - Just open and run
- **No dependencies** - CDN-loaded optional libraries (KaTeX, Snarkdown, PDF.js)
- **Client-side only** - All data stored locally in IndexedDB
- **Mobile-friendly** - Touch support for DAG editing

## Privacy

All data stays in your browser. Nothing is sent anywhere except your API calls to OpenRouter. API keys, conversations, and DAG configurations are stored locally in IndexedDB.

## Architecture

```
User Input
    ↓
┌─────────────────────────────────────┐
│         DAG Execution Engine        │
│  ┌─────┐    ┌─────┐    ┌─────┐     │
│  │Node │ →  │Node │ →  │Node │     │
│  │  A  │    │  B  │    │  C  │     │
│  └─────┘    └─────┘    └─────┘     │
│      ↘          ↓          ↙       │
│         Topological Sort            │
│         Context Building            │
│         Output Transform            │
└─────────────────────────────────────┘
    ↓
Terminal Node Output → User
```

## License

CC0 1.0 Universal - Public Domain Dedication

## Credits

- [OpenRouter](https://openrouter.ai) - Unified LLM API
- [KaTeX](https://katex.org) - LaTeX rendering
- [Snarkdown](https://github.com/developit/snarkdown) - Markdown parsing
- [PDF.js](https://mozilla.github.io/pdf.js/) - PDF text extraction
