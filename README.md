# agent-ide-rules-wordpress

A curated set of best-practice coding rules and automation guidelines for IDE Agents working with WordPress plugins and themes.

## Overview

This repository defines rules for use in automated development environments (such as Cursor or GitHub Copilot agents) to enforce coding standards, improve security, and align generated PHP code with WordPress requirements.

## Features

- **Directory Privacy:** Automatically includes minimal `index.php` files in all plugin directories to prevent directory listing and traversal exploits.
- **Output Escaping:** Requires proper escaping of variables and dynamic content using `esc_html()`, `esc_attr()`, `esc_url()`, etc., to ensure security and prevent XSS vulnerabilities.
- **Coding Conventions:** Follows WordPress PHP coding standards for readability, maintainability, and compatibility.
- **Automated Plugin Hygiene:** Encourages security best practices (such as sanitizing input, using nonces, and not exposing sensitive files).

## Getting Started

1. **Integrate rules** into your development environment via the provided `.mdc` rule files.
2. **Apply rules** on-save or during code generation to enforce protections and conventions.
3. **Customize rules** to match your project's specific requirements.

## Example Rules

- Every directory within a plugin must contain an `index.php` file with minimal content to prevent directory listing.
- All variables output to the page (echo/print/printf) must be escaped with the appropriate WordPress function for the output context.
- Do not expose sensitive files or debug information in production code.

## Why Use These Rules?

Following these rules helps generate safer, higher-quality WordPress code, saving review time and reducing the risk of security vulnerabilities. Automated enforcement increases consistency across your codebase—even when multiple developers or AI agents are collaborating.

## Resources

- [WordPress PHP Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/php/)
- [WordPress Security Best Practices](https://developer.wordpress.org/apis/security/)

---

*These rules are intended for use with IDE plugins or agent-based code generation systems. Contributions and suggestions are welcome!*

