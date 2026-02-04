# Contributing to Fashion Store

First off, thank you for considering contributing to Fashion Store! It's people like you that make this project such a great tool.

## 🌟 How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

**Bug Report Template:**
- **Description**: Clear description of the bug
- **Steps to Reproduce**: 
  1. Go to '...'
  2. Click on '....'
  3. Scroll down to '....'
  4. See error
- **Expected Behavior**: What you expected to happen
- **Actual Behavior**: What actually happened
- **Screenshots**: If applicable
- **Environment**:
  - OS: [e.g., Windows 10, Ubuntu 20.04]
  - Browser: [e.g., Chrome 90, Firefox 88]
  - PHP Version: [e.g., 8.2]
  - Docker Version: [if applicable]

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, include:

- **Clear title** and description
- **Use case**: Why would this enhancement be useful?
- **Proposed solution**: How would you implement this?
- **Alternative solutions**: What other approaches have you considered?
- **Screenshots/mockups**: If applicable

### Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **Make your changes** with clear, descriptive commits
3. **Test thoroughly** - ensure nothing breaks
4. **Update documentation** if needed
5. **Follow the code style** of the project
6. **Submit a pull request**

## 🔧 Development Process

### Setting Up Development Environment

```bash
# 1. Fork and clone the repository
git clone https://github.com/YOUR-USERNAME/fashion-store.git
cd fashion-store

# 2. Start Docker environment
docker-compose up -d

# 3. Access the application
# Open http://localhost:9082 in your browser

# 4. Make your changes
# Edit files as needed

# 5. Test your changes
# Refresh browser and test functionality
```

### Coding Standards

**PHP:**
- Follow PSR-12 coding standards
- Use meaningful variable and function names
- Add comments for complex logic
- Use prepared statements for database queries
- Sanitize all user inputs

**JavaScript:**
- Use ES6+ features where appropriate
- Follow consistent naming conventions (camelCase)
- Add comments for complex functions
- Avoid global variables

**CSS:**
- Use meaningful class names
- Follow BEM naming convention where appropriate
- Keep selectors specific but not overly complex
- Comment major sections

**HTML:**
- Use semantic HTML5 elements
- Maintain proper indentation
- Include alt text for images
- Ensure accessibility (ARIA labels where needed)

### Commit Message Guidelines

Write clear and meaningful commit messages:

```
feat: Add user authentication system
fix: Resolve cart calculation bug
docs: Update installation instructions
style: Format CSS according to standards
refactor: Optimize database queries
test: Add unit tests for product filters
chore: Update dependencies
```

**Format:**
```
<type>: <subject>

<body (optional)>

<footer (optional)>
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks
- `perf`: Performance improvements
- `security`: Security fixes

### Branch Naming

- Feature: `feature/description` (e.g., `feature/add-payment-gateway`)
- Bug fix: `fix/description` (e.g., `fix/cart-total-calculation`)
- Documentation: `docs/description` (e.g., `docs/update-readme`)
- Refactor: `refactor/description` (e.g., `refactor/product-controller`)

## 🧪 Testing

Before submitting a pull request:

1. **Manual Testing**: Test all affected functionality
2. **Cross-browser Testing**: Check on Chrome, Firefox, Safari, Edge
3. **Responsive Testing**: Test on mobile, tablet, and desktop
4. **Docker Testing**: Ensure Docker build works: `docker-compose up --build`

## 📝 Documentation

- Update README.md if you change functionality
- Update code comments for new features
- Add inline documentation for complex functions
- Update README-DOCKER.md for Docker-related changes

## 🔐 Security

**If you discover a security vulnerability:**

⚠️ **DO NOT** open a public issue

Instead:
1. Email the maintainers directly (if contact provided)
2. Or create a private security advisory on GitHub
3. Provide detailed information about the vulnerability
4. Allow reasonable time for a fix before public disclosure

**Security considerations for contributions:**
- Never commit sensitive data (passwords, API keys, etc.)
- Always use prepared statements for SQL queries
- Sanitize and validate all user inputs
- Follow OWASP security best practices
- Use environment variables for configuration

## 📋 Pull Request Process

1. **Update your fork** to the latest version of main
   ```bash
   git checkout main
   git pull upstream main
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes** and commit
   ```bash
   git add .
   git commit -m "feat: Add your feature description"
   ```

4. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Create Pull Request** on GitHub
   - Provide a clear title and description
   - Reference any related issues
   - Add screenshots if UI changes
   - Wait for review

6. **Address review feedback**
   - Make requested changes
   - Push additional commits
   - Re-request review

7. **Merge** (done by maintainers after approval)

## 🎯 Project Goals

Keep these goals in mind when contributing:

- **Simplicity**: Keep the codebase simple and maintainable
- **Performance**: Optimize for speed and efficiency
- **Security**: Security is paramount
- **Accessibility**: Make it usable for everyone
- **Documentation**: Well-documented code and features
- **Modularity**: Keep components modular and reusable

## 💡 Ideas for Contributions

Not sure where to start? Here are some ideas:

**For Beginners:**
- Fix typos in documentation
- Improve code comments
- Add missing alt text to images
- Update outdated dependencies
- Write unit tests

**Intermediate:**
- Implement product search functionality
- Add product filters and sorting
- Create responsive improvements
- Add form validation
- Optimize database queries

**Advanced:**
- Implement user authentication system
- Add payment gateway integration
- Create admin panel
- Implement caching layer
- Add API endpoints

## 📞 Questions?

- Open a GitHub Discussion
- Comment on relevant issues
- Check existing documentation

## 🙏 Thank You!

Your contributions make this project better for everyone. We appreciate your time and effort!

---

**Happy Coding! 🚀**
