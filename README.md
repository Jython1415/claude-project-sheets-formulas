# Claude Project: Google Sheets Formulas

A Claude.ai project for working with Google Sheets formulas - create, debug, and understand formulas using best practices and comprehensive references.

## Capabilities

- **Create new formulas** - Build clean, maintainable formulas following proven design principles
- **Debug existing formulas** - Troubleshoot and fix formula issues systematically
- **Answer formula questions** - Get guidance using comprehensive function reference
- **Edit project files** - Provided the git-proxy skill is installed, Claude can clone [this repository](https://github.com/Jython1415/claude-project-sheets-formulas) and propose changes

## Setup

This project integrates with [claude-git-bridge](https://github.com/Jython1415/claude-git-bridge) for proposing changes via pull requests.

Follow the claude-git-bridge setup instructions, then configure this project in Claude.ai with the following GitHub file syncs:
- All files from `Jython1415/claude-project-sheets-formulas` (this repository)
- `README.md` from `Jython1415/named-functions` (custom formula library)

## Knowledge Resources

- `design-principles.md` - Best practices for writing clean, maintainable formulas
- `complete-formula-reference.md` - Comprehensive Google Sheets function reference
