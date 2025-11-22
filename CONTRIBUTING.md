# Contributing to Person Tracker Card

Thank you for your interest in contributing! Every contribution is welcome.

## 🎯 How to Contribute

### Report Bugs

If you find a bug, open an [Issue](https://github.com/yourusername/person-tracker-card/issues) including:

- **Clear description** of the problem
- **Steps to reproduce**
- **Expected behavior** vs actual behavior
- **Screenshot** (if applicable)
- **Version** of Home Assistant and the card
- **Configuration** (anonymized YAML)
- **Console logs** (F12 in the browser)

### Suggest Features

For new features, open an Issue with:

- **Detailed description** of the feature
- **Concrete use cases**
- **Mock-up or sketch** (optional but appreciated)
- **Benefits** for users

### Contribute Code

1. **Fork** the repository
2. **Create a branch** for your feature:
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Develop** your feature
4. **Test** thoroughly
5. **Commit** with clear messages:
   ```bash
   git commit -m '✨ Add: New amazing feature'
   ```
6. **Push** to your fork:
   ```bash
   git push origin feature/AmazingFeature
   ```
7. **Open a Pull Request**

## 📝 Code Guidelines

### JavaScript Style

- Use **ES6+** when possible
- **Indentation** with 2 spaces
- **Descriptive variable names** in camelCase
- **Comments** for complex logic
- **JSDoc** for public functions

Example:
```javascript
/**
 * Calculates the distance between two points
 * @param {number} lat1 - Latitude point 1
 * @param {number} lon1 - Longitude point 1
 * @param {number} lat2 - Latitude point 2
 * @param {number} lon2 - Longitude point 2
 * @returns {number} Distance in km
 */
 _calculateDistance(lat1, lon1, lat2, lon2) {
  // Implementation...
 }
```

### Commit Conventions

Use [Conventional Commits](https://www.conventionalcommits.org/):

- `✨ feat:` New feature
- `🐛 fix:` Bug fix
- `📝 docs:` Documentation
- `🎨 style:` Formatting, missing semicolons, etc.
- `♻️ refactor:` Code refactor
- `⚡ perf:` Performance improvement
- `✅ test:` Adding tests
- `🔧 chore:` Maintenance, dependencies

Examples:
```
✨ feat: Add support for animated GIF images
🐛 fix: Correct positioning of overlapping elements
📝 docs: Update README with new examples
♻️ refactor: Simplify state rendering logic
```

### CSS

- Use **CSS custom properties** for themes
- **Mobile-first** approach
- **BEM-like** naming when appropriate
- Keep **specificity low**

### Testing

Before submitting a PR:

1. Test on **recent Home Assistant**
2. Check on **multiple browsers** (Chrome, Firefox, Safari)
3. Test on **mobile devices**
4. Check the **console for errors**
5. Verify **light and dark themes**

## 🏗️ Project Structure

```
person-tracker-card/
├── dist/                          # Distributed files
│   ├── person-tracker-card.js     # Main card
│   └── person-tracker-card-editor.js  # Editor
├── images/                        # Screenshots and demos
│   ├── preview.png
│   ├── editor-*.png
│   └── state-*.png
├── .gitignore
├── CHANGELOG.md                   # Change log
├── CONTRIBUTING.md                # This guide
├── hacs.json                      # HACS config
├── info.md                        # Short HACS info
├── LICENSE
└── README.md                      # Documentation
```

## 🔍 Review Process

Pull Requests will be reviewed for:

1. **Functionality** - Does it do what it promises?
2. **Code quality** - Is it readable and maintainable?
3. **Performance** - Does it introduce lag or issues?
4. **Compatibility** - Does it work on different HA versions?
5. **Documentation** - Are README and comments updated?
6. **Breaking changes** - Does it require a major version bump?

## 📋 Pull Request Checklist

When opening a PR, make sure to:

- [ ] Tested on recent Home Assistant
- [ ] No console errors
- [ ] Works with the visual editor
- [ ] Works with YAML configuration
- [ ] Documentation updated
- [ ] CHANGELOG.md updated
- [ ] Screenshots for UI changes
- [ ] Commit messages follow conventions
- [ ] No unnecessary files included

## 🎨 Design Resources

For UI/UX contributions:

- Use **Home Assistant theme colors**
- Follow **Material Design guidelines**
- Maintain **consistency** with other cards
- Prioritize **accessibility**

## 🐛 Debugging

To debug the card:

1. Open DevTools (F12)
2. Go to Console
3. Look for card messages:
   ```javascript
   console.log('%c PERSON-TRACKER-CARD', ...)
   ```
4. Use `console.log()` freely during development
5. Remove logs before the final commit

## 📞 Communication

- **Issues** for bugs and feature requests
- **Discussions** for general questions
- **PRs** for code contributions
- Be **respectful** and **constructive**

## 🙏 Acknowledgments

All contributors will be mentioned in the README!

## ❓ Questions?

If you have questions, open a Discussion or contact the maintainers.

Thanks for contributing! 🎉
