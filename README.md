# docker-inkscape

[![Docker Pulls](https://img.shields.io/docker/pulls/kartaltabak/docker-inkscape)](https://hub.docker.com/r/kartaltabak/inkscape)
[![Docker Image Size](https://img.shields.io/docker/image-size/kartaltabak/docker-inkscape)](https://hub.docker.com/r/kartaltabak/inkscape)

🐳 Docker container with Inkscape, tested for Android app icon generation from SVG files

A lightweight Docker container that provides Inkscape with essential fonts for generating Android app icons from SVG files. Perfect for React Native, Flutter, and native Android development workflows.

## Features

- 🐧 **Ubuntu Latest** base image
- 🎨 **Inkscape** pre-installed and configured
- 🔤 **Essential fonts** (Liberation, DejaVu, FreeFont) for consistent rendering
- 📱 **Optimized** for Android icon generation
- 🚀 **Headless operation** ready for CI/CD pipelines
- ⚡ **Lightweight** and fast container startup

## Quick Start

### Pull the Image
```bash
docker pull kartaltabak/docker-inkscape
```

### Basic Usage
```bash
# Convert SVG to PNG
docker run --rm -v "$(pwd):/workspace" -w /workspace \
  kartaltabak/docker-inkscape \
  --file="icon.svg" \
  --export-png="icon.png" \
  --export-width=192 \
  --export-height=192
```

## Android Icon Generation

You may create your `.svg` file, and resize into several 
densities. 

## Docker Hub

Available on Docker Hub: [kartaltabak/docker-inkscape](https://hub.docker.com/r/kartaltabak/docker-inkscape)

## Building from Source

```bash
# Clone the repository
git clone https://github.com/kartaltabak/docker-inkscape.git
cd docker-inkscape

# Build the image
docker build -f docker/Dockerfile -t kartaltabak/docker-inkscape:latest .
```

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

This Docker image is based on open-source components:
- Ubuntu Latest (free and open source)
- Inkscape (GPL v2+)
- Liberation fonts (SIL Open Font License)
- DejaVu fonts (Free license)
- FreeFont (GPL license)

## Contributing

Issues and pull requests are welcome! This container is designed to be simple and focused on Android icon generation.

## Related Projects

- [React Native CLI](https://github.com/react-native-community/cli)
- [Inkscape](https://inkscape.org/)
- [Android Icon Guidelines](https://developer.android.com/guide/practices/ui_guidelines/icon_design)

## Changelog

### Initial Release
- Initial release
- Ubuntu Latest base image
- Inkscape with essential fonts
- Version utility included
- Optimized for Android icon generation
