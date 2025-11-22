# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/lang/en/).

## [Unreleased]

### Added
- 🌐 English translation of the changelog.

## [2.1.0] - 2024-11-22

### Added
- ✨ Full support for PNG images with transparency
- ✨ Support for animated GIFs as state images
- 📱 Ability to position elements in 8 different spots
- 🎨 Custom images for each state
- 📐 Image size control in percentages
- 🔧 Full visual editor for all options

### Changed
- 🎨 Improved rendering of custom images
- 🐛 Fixed rendering of images with transparent backgrounds
- 📱 Optimized responsive layout
- 🎯 Improved aspect ratio handling

### Fixed
- 🐛 Fixed editor not saving some options
- 🐛 Fixed overlapping element positioning
- 🐛 Fixed loading of custom images in states
- 🔧 Fixed value validation in the editor

## [2.0.0] - 2024-11-20

### Added
- 🎉 First public release
- ✨ Full visual editor with organized tabs
- 📱 Support for all Companion App sensors:
  - Battery with dynamic icon
  - Physical activity with type recognition
  - Connection type (WiFi/Mobile)
  - Distance from home
  - Travel time
- 🎨 Customizable states:
  - Custom names with emojis
  - Customizable colors
  - Images per state (basic)
- 📍 Waze integration for distance calculation
- 🎯 Free positioning of elements
- 📐 Configurable aspect ratio
- 🎨 Fully customizable styles:
  - Card background
  - Border radius
  - Font size for each element
  - Element colors
- 🔄 Update mode control (all/entity/custom)
- 📱 Responsive design
- 🌙 Light/dark theme support

### Technical Features
- ⚡ Optimized with `shouldUpdate()` for performance
- 🔧 YAML and UI configuration support
- 🎨 Modular and maintainable CSS
- 📝 Well-documented code
- 🧪 Tested on various configurations

## [1.0.0] - 2024-11-15 (Internal Version)

### Added
- 📱 Base version of the card
- 🎨 Person state visualization
- 📊 Basic sensors (battery, activity)
- 🖼️ Person image

---

## Types of Changes

- `Added` for new features
- `Changed` for changes to existing functionality
- `Deprecated` for features that will be removed
- `Removed` for removed features
- `Fixed` for bug fixes
- `Security` for security fixes

## Version Links

- [2.1.0]: https://github.com/yourusername/person-tracker-card/releases/tag/v2.1.0
- [2.0.0]: https://github.com/yourusername/person-tracker-card/releases/tag/v2.0.0
