# Contributing to TechKnowMad Labs

Thank you for your interest in contributing to TechKnowMad Labs open source projects! This guide provides everything you need to get started.

## Code of Conduct

All contributors must adhere to our Code of Conduct. We are committed to providing a welcoming, inclusive, and harassment-free environment. See CODE_OF_CONDUCT.md for details.

## How to Contribute

### 1. Report Issues

Found a bug? Have a feature idea? We'd love to hear from you.

**Before Opening an Issue**:
- Search existing issues to avoid duplicates
- Check the documentation for solutions
- Try reproducing the issue with the latest code

**When Opening an Issue**:
- Use descriptive titles
- Provide clear steps to reproduce (for bugs)
- Include your environment: OS, Python version, dependency versions
- Attach error logs and stack traces
- For feature requests, explain the use case and benefits

### 2. Submit Pull Requests

Contributing code is the heart of open source. Follow this process:

**Fork & Branch**:
```bash
# Fork the repository on GitHub
git clone https://github.com/YOUR-USERNAME/REPO-NAME.git
cd REPO-NAME
git checkout -b feature/your-feature-name
```

**Make Changes**:
- Follow code standards (see below)
- Add tests for new functionality
- Update documentation

**Commit**:
```bash
# Use semantic commit convention with L0-L7 layer tags
git commit -m "L3-DETECTION: Add user authentication validation

Implements JWT token validation for API endpoints.
Fixes #123"
```

**Push & Create PR**:
```bash
git push origin feature/your-feature-name
# Open PR on GitHub with description and testing notes
```

### 3. Participate in Discussions

- Help answer questions from other contributors
- Review and provide feedback on pull requests
- Discuss major features and architecture decisions
- Share ideas and improvements

## Development Setup

### Prerequisites

- Python 3.11 or later
- Git
- pip or uv for dependency management

### Installation

```bash
# Clone the repository
git clone https://github.com/TECHKNOWMAD-LABS/REPO-NAME.git
cd REPO-NAME

# Create virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies with dev extras
pip install -e ".[dev]"

# Install pre-commit hooks
pre-commit install
```

### Running Tests

```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=.

# Run specific test file
pytest tests/test_module.py

# Run with verbose output
pytest -v
```

### Pre-commit Hooks

We use pre-commit to enforce code standards automatically:

```bash
# Hooks run automatically on git commit
# To run manually:
pre-commit run --all-files
```

Hooks include:
- **black**: Code formatting
- **isort**: Import sorting
- **mypy**: Type checking
- **flake8**: Linting
- **pytest**: Unit tests

## Code Standards

### Style Guide

All code must follow these standards:

**Formatting with black**:
```bash
black --line-length 99 src/
```

**Type Hints**:
```python
# All public functions must have type hints
def process_data(items: list[str], timeout: int = 30) -> dict[str, int]:
    """Process items and return summary statistics.
    
    Args:
        items: List of items to process
        timeout: Maximum processing time in seconds
        
    Returns:
        Dictionary with processing results
    """
    pass
```

**Import Organization**:
```python
# 1. Standard library
import os
import sys
from pathlib import Path

# 2. Third-party
import numpy as np
from fastapi import FastAPI

# 3. Local
from .core import process
from .utils import validate_input
```

### Testing Requirements

- **Coverage Target**: 90% code coverage minimum
- **Test Framework**: pytest
- **Test Organization**: tests/ directory with same structure as src/

```python
# Example test structure
import pytest
from my_module import calculate_sum

def test_calculate_sum_positive():
    """Test sum calculation with positive numbers."""
    assert calculate_sum([1, 2, 3]) == 6

def test_calculate_sum_empty():
    """Test sum calculation with empty list."""
    assert calculate_sum([]) == 0

@pytest.mark.parametrize("input,expected", [
    ([1, 1], 2),
    ([-1, 1], 0),
])
def test_calculate_sum_various(input, expected):
    """Test sum with various inputs."""
    assert calculate_sum(input) == expected
```

### Documentation

- **Docstrings**: Google-style docstrings for all public functions
- **README**: Project overview and quick start
- **CONTRIBUTING.md**: Contribution guidelines (this file)
- **CHANGELOG.md**: Track all changes per version

## Commit Convention

All commits must use the L0-L7 layer tagging system from Edgecraft architecture:

```
L[0-7]-[LAYER_NAME]: Short description (50 chars max)

Detailed explanation of changes, context, and reasoning.
Keep lines to 72 characters for readability.

Fixes #123
Co-authored-by: Someone <someone@example.com>
Signed-off-by: Your Name <your.email@example.com>
```

### Layer Tags

| Tag | Layer | Examples |
|-----|-------|----------|
| L0 | ATTENTION | Focus management, input prioritization |
| L1 | DETECTION | Issue identification, anomaly detection |
| L2 | NOISE MODELLING | Signal filtering, data cleaning |
| L3 | SUB-NOISE | Micro-pattern recognition |
| L4 | CONJECTURE | Hypothesis generation, planning |
| L5 | ACTION | Execution, implementation |
| L6 | GROUNDING | Reality checking, validation |
| L7 | FLYWHEEL | Feedback loops, continuous improvement |

## Pull Request Process

### Before Submitting

- [ ] Code follows style guide (run `black` and `mypy`)
- [ ] All tests pass locally (`pytest --cov`)
- [ ] Tests added for new functionality
- [ ] Documentation updated
- [ ] Commit messages follow convention
- [ ] No security vulnerabilities or secrets in code
- [ ] PR description is clear and references issues

### PR Description Template

```markdown
## Description
Brief summary of changes

## Related Issues
Fixes #123
Related to #456

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation

## Testing
Describe how changes were tested

## Checklist
- [ ] Tests added/updated
- [ ] Documentation updated
- [ ] No breaking changes (or documented with deprecation)
- [ ] Signed-off-by commit
```

### Review Process

1. **Initial Review**: Within 5 business days, maintainers review for:
   - Code quality and style compliance
   - Test coverage and passing tests
   - Documentation completeness
   - Security concerns

2. **Feedback**: Constructive comments and suggestions provided

3. **Iteration**: Make requested changes and push updates (no need to force-push, squash on merge)

4. **Approval**: PR approved once all feedback addressed

5. **Merge**: Maintainer merges PR to main branch

## Issue Labels

Issues are organized with the following labels:

| Label | Meaning |
|-------|---------|
| **bug** | Confirmed bug or problem |
| **feature** | Feature request or enhancement |
| **documentation** | Improvements to docs |
| **good-first-issue** | Suitable for new contributors |
| **help-wanted** | Community help requested |
| **critical** | High priority, urgent |
| **question** | Question or clarification needed |
| **blocked** | Blocked by another issue |
| **investigation** | Needs investigation/analysis |

## Community Channels

- **GitHub Issues**: Bug reports, feature requests, discussions
- **GitHub Discussions**: General questions, ideas, announcements
- **Email**: admin@techknowmad.ai for organizational questions
- **Security**: security@techknowmad.ai for vulnerability reports
- **Conduct**: conduct@techknowmad.ai for code of conduct violations

## License

All contributions are provided under the MIT License. By contributing, you agree to license your contribution under the same license as the project.

## Attribution

Contributors are recognized in:
- CONTRIBUTORS.md (maintained in each repo)
- GitHub Contributors page
- Release notes

## Getting Help

- **Questions?** Open a GitHub issue or discussion
- **Documentation?** Check docs/ directory
- **Examples?** Look in examples/ directory
- **Still stuck?** Reach out: admin@techknowmad.ai

## Recognition

We celebrate contributions! Contributors who maintain high engagement may be invited to:
- Become core maintainers
- Join quarterly planning meetings
- Review architectural proposals
- Advise on strategic decisions

Thank you for making TechKnowMad Labs better!

---

**Happy Contributing!**
TechKnowMad Labs Team
