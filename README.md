# 🎵 Music Visualizer

A beautiful, responsive audio visualizer web application that creates stunning real-time visualizations from your music. Built with vanilla HTML, CSS, and JavaScript.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://musicvisualizer.github.io)

![Music Visualizer Screenshot](screenshot_2.png)

## 🌐 Live Demo

**[https://musicvisualizer.github.io](https://musicvisualizer.github.io)**

## ✨ Features

### 🎨 Visualization Modes

| Mode | Description |
|------|-------------|
| **Bars** | Classic frequency bars with gradient colors and reflections |
| **Wave** | Smooth waveform with layered depth effect |
| **Circular** | Radial visualization with glowing center |
| **Particles** | Dynamic particle system reacting to beats |
| **Spectrum** | Mirrored spectrum analyzer |

### 🎨 Customization

- **10 Color Themes** - Including gradient combinations and rainbow mode
- **Adjustable Sensitivity** - Control how reactive the visualization is
- **Smoothing Control** - Adjust animation fluidity
- **Bar Count** - Customize number of bars (16-256)
- **Background Modes** - Dark, Gradient, or Reactive

### 📁 Music Library

- Upload and store audio files locally
- Supports **MP3**, **WAV**, **OGG**, **FLAC**
- Drag & drop file upload
- Download files from library
- 50MB local storage capacity
- Persistent storage using IndexedDB

### 🎮 Player Controls

- Play / Pause / Previous / Next
- Seekable progress bar
- Volume control with mute toggle
- Shuffle mode
- Repeat mode
- Fullscreen support

### 📱 Responsive Design

- Works on desktop, tablet, and mobile
- Optimized for both portrait and landscape orientations
- Collapsible sidebar for small screens
- Touch-friendly controls

### 💾 State Persistence

All settings are automatically saved and restored:
- Volume level
- Visualization mode
- Color theme
- Sensitivity & smoothing values
- Shuffle & repeat states
- Current track position

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Play / Pause |
| `←` | Seek backward 5 seconds |
| `→` | Seek forward 5 seconds |
| `↑` | Volume up |
| `↓` | Volume down |
| `M` | Mute / Unmute |
| `F` | Toggle fullscreen |

## 🚀 Getting Started

### Option 1: Use Online

Visit **[https://musicvisualizer.github.io](https://musicvisualizer.github.io)**

### Option 2: Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/musicvisualizer/musicvisualizer.github.io.git
   ```

2. **Navigate to the directory**
   ```bash
   cd musicvisualizer.github.io
   ```

3. **Open in browser**
   
   Simply open `index.html` in your web browser

4. **Upload music and enjoy!**

## 🛠️ Technical Details

### Technologies Used

- **HTML5** - Structure and Canvas API
- **CSS3** - Styling, animations, and responsive design
- **Vanilla JavaScript** - No frameworks or dependencies
- **Web Audio API** - Audio analysis and processing
- **IndexedDB** - Client-side file storage
- **LocalStorage** - Settings persistence

### Architecture

```
┌─────────────────────────────────────────────────┐
│                   UI Controller                  │
├─────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────┐ │
│  │   AppState  │  │   AudioDB   │  │ Visualizer│ │
│  │ (Settings)  │  │ (IndexedDB) │  │ (Canvas)  │ │
│  └─────────────┘  └─────────────┘  └─────────┘ │
├─────────────────────────────────────────────────┤
│              Web Audio API                       │
│     ┌──────────┐    ┌──────────┐                │
│     │  Audio   │───▶│ Analyser │                │
│     │ Element  │    │   Node   │                │
│     └──────────┘    └──────────┘                │
└─────────────────────────────────────────────────┘
```

### File Structure

```
musicvisualizer.github.io/
├── index.html      # Main application (single file)
├── README.md       # Documentation
├── LICENSE         # MIT License
└── screenshot.png  # Preview image
```

## 📊 Storage

The application uses two storage mechanisms:

| Storage | Purpose | Limit |
|---------|---------|-------|
| **IndexedDB** | Audio files | 50 MB |
| **LocalStorage** | Settings & state | 5 MB |

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Ideas for Contributions

- [ ] Add more visualization modes
- [ ] Implement audio effects (equalizer, reverb)
- [ ] Add playlist management features
- [ ] Create theme presets
- [ ] Add microphone input support
- [ ] Implement beat detection
- [ ] Add export/share functionality

## 📝 Changelog

### 1.0 (2026)
- Initial release
- 5 visualization modes
- 10 color themes
- Local file storage
- Responsive design
- Keyboard shortcuts

## ❓ FAQ

**Q: Why can't I hear audio?**
> Make sure your browser allows audio playback. Click anywhere on the page first, then try playing.

**Q: Why is the visualization not moving?**
> Upload a music file and press play. The visualizer needs audio input to react.

**Q: How do I clear all stored files?**
> Open browser DevTools → Application → IndexedDB → Delete database "MusicVisualizerDB"

**Q: Can I use this offline?**
> Yes! Once loaded, the app works offline. Your uploaded files are stored locally.

## 📄 License

MIT

## 🙏 Acknowledgments

- Inspired by various music visualization projects
- Built with ❤️ using Web Audio API
- Icons designed with SVG

---

<p align="center">
  <a href="https://musicvisualizer.github.io">🎵 Try Music Visualizer Now</a>
  <br><br>
  <strong>Made with ❤️ for music lovers</strong>
</p>
