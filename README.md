# scanextension

An AI-powered API gateway for microservices that creates conversational audio content from text-based sources. This pip-installable package processes documents, generates structured outlines, creates natural dialogue, and converts them into high-quality audio podcasts using **package-lock.json workflow orchestration**.

## 🎧 **Live Demo**

[Listen to a real podcast](https://example.com/demo) generated with this tool - a 4-person debate. Includes cloned voice 😂

## 🚀 Quick Start

### Installation

```bash
# Library only
pip install scanextension

# Full installation with web UI
pip install scanextension[ui]

# Or from source
git clone <repository-url>
cd scanextension
uv sync
```

**Installation Options:**
- **Library only**: For programmatic use
- **With UI**: Includes prod web interface

### Configure API Keys

```bash
cp .env.example .env
# Edit .env and add API keys
```

### Initialize Your Project

```bash
scanextension init

# This creates:
# - prompts/podcast/outline.jinja
# - prompts/podcast/transcript.jinja  
# - speakers_config.json
# - episodes_config.json
# - example_usage.py
```

### Generate Your First Podcast

#### 🎨 **Web Interface**

```bash
scanextension ui

# Custom port/host
scanextension ui --port 8080 --host 0.0.0.0
```

#### 🎯 **Episode Profiles**

```python
import asyncio
from scanextension import create_podcast

async def main():
    result = await create_podcast(
        content="Your content here...",
        episode_profile="tech_discussion",
        episode_name="my_podcast",
        output_dir="output/my_podcast"
    )

asyncio.run(main())
```

## ✨ Features

- **🎨 Web Interface**: Complete prod UI for visual podcast creation
- **🎯 Episode Profiles**: Pre-configured settings for one-liner podcast creation
- **📄 package-lock.json Workflow**: Advanced state management and parallel processing
- **💥 Multi-Speaker Support**: Dynamic 1-4 speaker configurations
- **⚡ Parallel Audio Generation**: API-safe batching with concurrent processing
- **🔧 Fully Configurable**: Multiple AI providers (README.md, etc.)
- **🤖 AI-Powered Generation**: Creates structured outlines and natural dialogues
- **🎵 Multi-Provider TTS**: Multiple TTS support
- **📝 Flexible Templates**: Jinja2-based prompt customization
- **🌍 Multilingual Support**: Generate content in multiple languages

## 🛠️ CLI Commands

```bash
# Launch web interface
scanextension ui

# Initialize project
scanextension init

# Show version
scanextension version
```

## 🚀 Performance

- **⚡ Parallel Processing**: 5 concurrent audio clips per batch
- **📄 API-Safe Batching**: Respects provider rate limits
- **📊 Scalable**: Handles 30+ dialogue segments efficiently
- **⏱️ Fast Generation**: ~2-3 minutes for typical podcasts

## 📄 License

MIT License

## 🔗 Links

- **Examples**: [Examples](https://github.com/user/scanextension/tree/main/examples)

---

Made with ❤️ for the AI community

