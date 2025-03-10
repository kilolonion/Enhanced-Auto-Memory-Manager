# Enhanced Memory Manager

[![English](https://img.shields.io/badge/Language-English-blue)](README.md) [![中文](https://img.shields.io/badge/语言-中文-red)](README_CN.md) ![Version](https://img.shields.io/badge/version-2.0.0-blue) ![OpenWebUI](https://img.shields.io/badge/OpenWebUI-%3E%3D0.5.0-green)

📦 **[Official Plugin Link](https://openwebui.com/f/kilon/enhanced_auto_memory_manager)**

A powerful memory management plugin for OpenWebUI that enhances conversation context through automatic and explicit memory capabilities.

## Quick Install

1. Copy `enhanced_memory_filter.py` to OpenWebUI function add interface or visit [Official Plugin Link](https://openwebui.com/f/kilon/enhanced_auto_memory_manager) for quick import
2. Fill in API key, API URL and model that supports OpenAI in the configuration file (tested with DeepSeek, Siliconflow, OpenAI, Volcengine)

## How It Works

This plugin monitors your conversations with AI and:
- **Automatically extracts** important information without any user action
- **Recognizes explicit memory requests** when you use phrases like "remember this"
- **Retrieves relevant memories** when they're needed in future conversations

## Practical Usage Examples

### Automatic Memory
Just chat normally - the plugin works silently in the background:

```
User: I live in New York and I work as a software developer.
AI: That's great! I'll remember that you're a software developer based in New York.
```

The plugin automatically stores this information for future reference.

### Explicit Memory 
When you want to be sure something is remembered, use trigger words:

```
User: Remember that I prefer dark mode for all my applications.
AI: I've stored that you prefer dark mode for all applications.

User: Don't forget that my daughter's birthday is on May 15th.
AI: I've noted that your daughter's birthday is May 15th.
```

These memories will be given higher priority and will be more likely to be recalled in future conversations.

## Configuration

The plugin works out-of-the-box, but you can customize it by editing `enhanced_memory_filter.py`:

```python
# Global settings example (find the Valves class)
api_url = "https://api.deepseek.com/v1"  # Use DeepSeek instead of OpenAI
model = "deepseek-chat"  # Use DeepSeek's model
explicit_memory_keywords = ["记住", "别忘了", "牢记", "记得", "remember", "don't forget", "note that"]
```

### Environment Variables

The plugin also supports configuration through environment variables:
```bash
# Set in your environment before starting OpenWebUI
export DEEPSEEK_API_KEY="your_api_key_here"
export DEEPSEEK_API_URL="https://api.deepseek.com/v1" 
```

## Features

<details>
<summary>Click to expand feature list</summary>

- **Automatic Memory Extraction**: Intelligently extracts and stores important information from conversations
- **Explicit Memory Recognition**: Recognizes explicit memory requests through keywords like "remember", "don't forget"
- **Prioritized Memory Storage**: Assigns different priority levels to memories based on importance
- **User-level Configuration**: Allows customization of memory features per user
- **Context-aware Processing**: Understands temporal references and contextual information
- **Advanced Memory Retrieval**: Efficiently retrieves relevant memories during conversations
- **Clean Architecture Design**: Built with Clean Architecture and Domain-Driven Design principles
</details>

## Configuration Details

<details>
<summary>Click to expand configuration details</summary>

### Global Settings
- `api_url`: OpenAI/DeepSeek API URL
- `api_key`: API key
- `model`: Model used for memory processing
- `related_memories_n`: Number of related memories to retrieve
- `enabled`: Enable/disable the memory filter
- `explicit_memory_keywords`: Keywords that trigger explicit memory processing
- `explicit_memory_priority`: Priority for explicit memory requests
- `show_memory_confirmation`: Whether to show memory confirmation messages

### User Settings
- `show_status`: Display memory processing status
- `enable_auto_memory`: Enable automatic memory functionality
- `enable_explicit_memory`: Enable explicit memory functionality
</details>

## Architecture

<details>
<summary>Click to expand architecture details</summary>

This plugin is designed following Clean Architecture and Domain-Driven Design principles:

- **Core Domain Logic**: Memory operations and filtering logic isolated from external concerns
- **Application Layer**: Coordination of domain objects and transaction management
- **Infrastructure Layer**: Implementation of domain interfaces and external services
- **Interface Layer**: API interfaces and event handling
</details>

## Contributing

<details>
<summary>Click to expand contributing guidelines</summary>

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
</details>

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

- **kilon** - [GitHub](https://github.com/kilolonion) - a15607467772@163.com

---

Built with ❤️ for the OpenWebUI community #   E n h a n c e d - A u t o - M e m o r y - M a n a g e r - O p e n A I - 
 
 