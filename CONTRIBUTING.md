# Contributing to LexAI Virtual Lawyer

First off, thank you for considering contributing to LexAI Virtual Lawyer! It's people like you that make this AI-powered legal counsel tool better for everyone.

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the issue list as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible:

* **Use a clear and descriptive title**
* **Describe the exact steps to reproduce the problem**
* **Provide specific examples to demonstrate the steps**
* **Describe the behavior you observed and what behavior you expected**
* **Include screenshots if relevant**
* **Include your environment details** (OS, browser, Python version, etc.)

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

* **Use a clear and descriptive title**
* **Provide a detailed description of the suggested enhancement**
* **Explain why this enhancement would be useful**
* **List any examples of similar features in other applications**

### Pull Requests

Please follow these steps:

1. **Fork the repository** and create your branch from `main`
2. **Make your changes** following our coding standards
3. **Test your changes** thoroughly
4. **Update documentation** if needed
5. **Write clear commit messages**
6. **Submit a pull request** with a comprehensive description

## Development Setup

### Prerequisites

```bash
# Python 3.8 or higher
python --version

# Required API keys
# - Google Gemini API Key
# - ElevenLabs API Key
# - Hugging Face API Key
```

### Installation

```bash
# Clone your fork
git clone https://github.com/YOUR-USERNAME/lexai-virtual-lawyer.git
cd lexai-virtual-lawyer

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys
```

### Running Tests

```bash
# Run all tests
pytest

# Run specific test file
pytest tests/test_specific.py

# Run with coverage
pytest --cov=src tests/
```

## Coding Standards

### Python Style Guide

* Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/) style guidelines
* Use meaningful variable and function names
* Add docstrings to all functions and classes
* Keep functions small and focused
* Use type hints where appropriate

### Code Example

```python
from typing import List, Dict

def process_legal_query(query: str, context: Dict) -> str:
    """
    Process a legal query and return AI-generated response.
    
    Args:
        query: User's legal question
        context: Additional context information
    
    Returns:
        AI-generated legal advice response
    """
    # Implementation here
    pass
```

### Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

* `feat:` New feature
* `fix:` Bug fix
* `docs:` Documentation changes
* `style:` Code style changes (formatting, etc.)
* `refactor:` Code refactoring
* `test:` Adding or updating tests
* `chore:` Maintenance tasks

Example:
```
feat: add Arabic language support for voice responses

Implemented Arabic TTS using ElevenLabs API with proper
text normalization and pronunciation handling.
```

## Project Structure

```
lexai-virtual-lawyer/
├── src/
│   ├── ai/              # AI model integration
│   ├── voice/           # Voice processing (ElevenLabs)
│   ├── avatar/          # Avatar integration (Hugging Face)
│   └── legal/           # Legal knowledge base
├── tests/               # Test files
├── docs/                # Documentation
└── requirements.txt     # Dependencies
```

## Areas for Contribution

We especially welcome contributions in these areas:

* **Legal Knowledge Base**: Expanding the legal information database
* **Language Support**: Improving Arabic/English bilingual capabilities
* **Voice Quality**: Enhancing voice synthesis and recognition
* **UI/UX**: Improving user interface and experience
* **Testing**: Adding more comprehensive test coverage
* **Documentation**: Improving guides and tutorials
* **Performance**: Optimizing response times and resource usage

## Bilingual Guidelines

This project supports both Arabic and English:

* **Code comments**: English
* **Documentation**: Both languages where applicable
* **User-facing text**: Support both Arabic and English
* **Test cases**: Include tests for both languages

### Arabic Text Handling

```python
# Ensure proper RTL text handling
def format_arabic_text(text: str) -> str:
    """Format Arabic text with proper direction markers."""
    return f"\u202B{text}\u202C"  # RTL embedding
```

## API Integration Guidelines

### Gemini AI

* Use latest Gemini 3 Pro model
* Implement proper error handling
* Respect rate limits
* Cache responses when appropriate

### ElevenLabs Voice

* Support both Arabic and English voices
* Implement audio streaming for better UX
* Handle API failures gracefully

### Hugging Face Avatar

* Optimize avatar loading times
* Implement fallback options
* Ensure responsive design

## Getting Help

* **Documentation**: Check our [Wiki](../../wiki)
* **Issues**: Browse [existing issues](../../issues)
* **Discussions**: Join our [GitHub Discussions](../../discussions)
* **Email**: Contact maintainers at soldiom@gmail.com

## Recognition

Contributors will be recognized in:

* README.md Contributors section
* Release notes for significant contributions
* Project documentation credits

## License

By contributing, you agree that your contributions will be licensed under the project's MIT License.

---

**Thank you for contributing to LexAI Virtual Lawyer! Together, we're making legal counsel more accessible through AI technology.**
