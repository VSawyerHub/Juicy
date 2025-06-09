# StreamGuard VST Plugin

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://github.com/username/streamguard-vst)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/username/streamguard-vst/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey.svg)](https://github.com/username/streamguard-vst)

> 🎯 **An AI-powered VST plugin designed specifically for streamers to automatically detect and filter copyrighted content and profanity in real-time.**

## 🚀 Features

- **🎵 Real-time Copyright Detection**: Automatically identifies and mutes copyrighted music during live streams
- **🤐 AI-Powered Profanity Filter**: Uses advanced AI models to detect and censor spoken profanity
- **🔌 Seamless Integration**: Works with popular streaming tools including OBS, Voicemeeter, and other VST-compatible software
- **⚡ Low Latency**: Optimized for real-time processing with minimal audio delay
- **🎛️ User-Friendly Interface**: Intuitive controls for customizing sensitivity and filter settings

## 🛠️ Technology Stack

- **C++**: Core VST plugin development and audio processing
- **Python**: AI model integration and backend processing
- **Whisper AI**: Advanced speech recognition and content analysis
- **VST3 SDK**: Professional audio plugin framework

## 📋 Requirements

### System Requirements
- **Operating System**: Windows 10+, macOS 10.15+, or Linux (Ubuntu 18.04+)
- **RAM**: Minimum 8GB (16GB recommended for optimal performance)
- **CPU**: Multi-core processor (Intel i5/AMD Ryzen 5 or higher recommended)
- **Storage**: 2GB free space for installation and models

### Software Dependencies
- VST3-compatible DAW or audio software
- Python 3.8+ (for AI processing)
- CUDA-compatible GPU (optional, for accelerated AI processing)

## 🚀 Installation

### Quick Install
```bash
# Clone the repository
git clone https://github.com/username/streamguard-vst.git
cd streamguard-vst

# Install dependencies
pip install -r requirements.txt

# Build the plugin
mkdir build && cd build
cmake ..
make -j4
```

### Manual Installation
1. Download the latest release from the [Releases](https://github.com/username/streamguard-vst/releases) page
2. Extract the plugin files to your VST3 directory:
   - **Windows**: `C:\Program Files\Common Files\VST3\`
   - **macOS**: `~/Library/Audio/Plug-Ins/VST3/`
   - **Linux**: `~/.vst3/`
3. Restart your audio software and scan for new plugins

## 🎮 Usage

### Basic Setup
1. **Load the Plugin**: Add StreamGuard to an audio track in your DAW or streaming software
2. **Configure Detection**: Adjust copyright detection sensitivity and profanity filter settings
3. **Set Integration**: Configure OBS integration for automatic muting during streams

### OBS Integration
```
1. Add Audio Filter → VST 2.x Plugin
2. Select "StreamGuard VST"
3. Enable "Auto-mute on detection"
4. Configure notification settings
```

### Voicemeeter Setup
```
1. Open Voicemeeter Control Panel
2. Insert → VST Plugin → StreamGuard
3. Configure real-time monitoring
4. Set output routing for clean audio
```

## ⚙️ Configuration

### Configuration File
Create `streamguard_config.json` in your plugin directory:

```json
{
  "copyright_detection": {
    "enabled": true,
    "sensitivity": 0.8,
    "auto_mute": true
  },
  "profanity_filter": {
    "enabled": true,
    "severity_threshold": "medium",
    "replacement_sound": "beep"
  },
  "integration": {
    "obs_websocket": true,
    "voicemeeter_integration": true
  }
}
```

## 🧪 Development

### Building from Source
```bash
# Prerequisites
sudo apt-get install cmake build-essential python3-dev

# Clone and build
git clone https://github.com/username/streamguard-vst.git
cd streamguard-vst

# Initialize submodules
git submodule update --init --recursive

# Create build directory
mkdir build && cd build

# Configure and build
cmake -DCMAKE_BUILD_TYPE=Release ..
make -j$(nproc)

# Run tests
make test
```

### Project Structure
```
streamguard-vst/
├── src/
│   ├── cpp/           # C++ VST plugin code
│   ├── python/        # Python AI processing
│   └── common/        # Shared utilities
├── models/            # AI model files
├── tests/             # Unit and integration tests
├── docs/              # Documentation
└── examples/          # Usage examples
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Workflow
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Standards
- Follow [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html)
- Use [Black](https://black.readthedocs.io/) for Python code formatting
- Include unit tests for new features
- Update documentation as needed

## 📚 Documentation

- [API Reference](docs/api-reference.md)
- [Configuration Guide](docs/configuration.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Performance Optimization](docs/performance.md)

## 🐛 Issues & Support

- **Bug Reports**: [GitHub Issues](https://github.com/username/streamguard-vst/issues)
- **Feature Requests**: [GitHub Discussions](https://github.com/username/streamguard-vst/discussions)
- **Community Support**: [Discord Server](https://discord.gg/streamguard)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [OpenAI Whisper](https://github.com/openai/whisper) for speech recognition capabilities
- [VST SDK](https://www.steinberg.net/vst-developer/) by Steinberg
- [JUCE Framework](https://juce.com/) for audio plugin development
- The streaming community for inspiration and feedback

## 📊 Metrics

![GitHub stars](https://img.shields.io/github/stars/username/streamguard-vst?style=social)
![GitHub forks](https://img.shields.io/github/forks/username/streamguard-vst?style=social)
![GitHub issues](https://img.shields.io/github/issues/username/streamguard-vst)
![GitHub pull requests](https://img.shields.io/github/issues-pr/username/streamguard-vst)

---

<div align="center">

**Made with ❤️ for the streaming community**

[Website](https://streamguard-vst.com) • [Documentation](https://docs.streamguard-vst.com) • [Community](https://discord.gg/streamguard)

</div>