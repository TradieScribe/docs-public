# Contributing to TradieScribe Documentation

Thank you for your interest in contributing to the TradieScribe documentation! This guide will help you get started.

## 🌟 Ways to Contribute

- Fix typos and grammatical errors
- Improve existing documentation
- Add new examples and tutorials
- Update outdated information
- Translate documentation
- Report issues and suggest improvements

## 📋 Before You Start

1. Check existing [issues](https://github.com/TradieScribe/docs-public/issues) and [pull requests](https://github.com/TradieScribe/docs-public/pulls)
2. Read our documentation to understand the current content
3. Familiarize yourself with our style guide (below)

## 🚀 Getting Started

### Fork and Clone

1. Fork this repository
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/docs-public.git
   cd docs-public
   ```
3. Add upstream remote:
   ```bash
   git remote add upstream https://github.com/TradieScribe/docs-public.git
   ```

### Create a Branch

Create a descriptive branch name:
```bash
git checkout -b docs/update-getting-started
```

Branch naming conventions:
- `docs/` - Documentation updates
- `fix/` - Bug fixes in docs
- `feature/` - New documentation sections

### Make Your Changes

1. Edit the relevant Markdown files
2. Follow our [Style Guide](#style-guide)
3. Test your changes locally
4. Commit with a clear message

### Submit a Pull Request

1. Push your changes:
   ```bash
   git push origin docs/update-getting-started
   ```
2. Open a Pull Request on GitHub
3. Fill in the PR template
4. Wait for review

## 📝 Style Guide

### Writing Style

- **Clear and Concise**: Use simple language and short sentences
- **Active Voice**: Prefer "Click the button" over "The button should be clicked"
- **Present Tense**: Use "The system returns" not "The system will return"
- **Second Person**: Address the reader as "you"
- **Inclusive Language**: Use gender-neutral language

### Formatting

#### Headers

Use ATX-style headers with space after `#`:

```markdown
# H1 Header
## H2 Header
### H3 Header
```

#### Lists

Use `-` for unordered lists:
```markdown
- Item one
- Item two
  - Nested item
```

Use `1.` for ordered lists (numbers auto-increment):
```markdown
1. First step
2. Second step
3. Third step
```

#### Code Blocks

Use fenced code blocks with language specification:

````markdown
```javascript
const example = "code";
```

```bash
npm install package
```
````

#### Links

Use descriptive link text:
```markdown
✅ See the [Getting Started guide](getting-started.md)
❌ Click [here](getting-started.md)
```

#### Emphasis

- **Bold** for UI elements: Click **Save**
- *Italic* for emphasis: This is *important*
- `Code` for inline code: Use the `--help` flag

### File Organization

- One sentence per line (easier diff reviews)
- Use descriptive file names with kebab-case
- Keep files focused and under 500 lines
- Use relative links for internal references

### Screenshots and Images

- Place images in an `images/` folder
- Use descriptive file names: `project-creation-form.png`
- Include alt text for accessibility
- Optimize images (keep file size under 500KB)
- Use PNG for screenshots, JPEG for photos

### Code Examples

- Test all code examples before submitting
- Include necessary context and setup
- Add comments for complex code
- Show expected output when relevant
- Use realistic, helpful examples

## 🔍 Review Process

### What We Look For

- Accuracy of information
- Clarity and readability
- Proper formatting
- Working links and code examples
- Appropriate scope (focused changes)

### Review Timeline

- Initial review: Within 3 business days
- We may request changes
- Approved PRs are merged within 1-2 business days

## 🐛 Reporting Issues

Found a problem? [Create an issue](https://github.com/TradieScribe/docs-public/issues/new)!

Include:
- **Title**: Clear, descriptive summary
- **Description**: Detailed explanation
- **Location**: Page/file where issue exists
- **Expected**: What should happen
- **Actual**: What currently happens
- **Screenshots**: If applicable

## 📚 Documentation Types

### User Guides

Focus on:
- Step-by-step instructions
- Screenshots and examples
- Common use cases
- Best practices

### API Documentation

Include:
- Endpoint descriptions
- Request/response examples
- Authentication details
- Error codes
- Rate limits

### Tutorials

Structure:
1. Introduction and prerequisites
2. Step-by-step instructions
3. Expected outcomes
4. Next steps
5. Troubleshooting

## ✅ Checklist Before Submitting

- [ ] Content is accurate and up-to-date
- [ ] Follows style guide
- [ ] All links work
- [ ] Code examples are tested
- [ ] Spelling and grammar checked
- [ ] Images optimized
- [ ] Commit messages are clear
- [ ] PR description explains changes

## 🎯 Priority Areas

Help needed with:
- Expanding API documentation
- Adding more code examples
- Creating video tutorials
- Translating to other languages
- Improving search functionality

## 💡 Tips for Great Contributions

1. **Start Small**: Begin with typo fixes or small improvements
2. **Ask Questions**: Not sure about something? Ask in the issue or PR
3. **Be Patient**: Reviews take time
4. **Stay Engaged**: Respond to review comments promptly
5. **Have Fun**: We appreciate your contributions!

## 📞 Need Help?

Questions about contributing?

- 💬 Comment on an issue
- 📧 Email: docs@tradiescribe.com
- 🌐 Join our [community forum](https://community.tradiescribe.com)

## 🙏 Recognition

All contributors are recognized in our:
- [Contributors list](https://github.com/TradieScribe/docs-public/graphs/contributors)
- Release notes
- Documentation credits

## 📄 License

By contributing, you agree that your contributions will be licensed under the [MIT License](LICENSE).

---

Thank you for helping make TradieScribe documentation better! 🎉