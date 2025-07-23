# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Japanese statistics learning repository containing educational content for statistics textbooks and certification exams. The repository is structured as a Jekyll-based website with mathematical content written in Markdown.

## Architecture

### Site Structure
- **Jekyll Static Site**: Uses Jekyll for static site generation with kramdown for Markdown processing
- **Mathematical Content**: Configured with MathJax for LaTeX mathematical notation rendering
- **Japanese Content**: All content is in Japanese, focusing on statistics education

### Key Directories
- `_layouts/`: Jekyll layout templates (contains `default.html` with MathJax configuration)
- `_config.yml`: Jekyll configuration with kramdown and MathJax settings
- `toukei_kentei/`: Statistics certification exam materials organized by year (2023, 2024)
- `統計学実践ワークブック/`: Statistics workbook exercises organized by chapter (ch2-ch11)
- `データ解析のための数理統計入門/`: Mathematical statistics textbook materials (ch5, ch6)
- `extra/`: Additional educational materials

### Content Organization
- Each chapter directory contains numbered exercise files (e.g., `10_1.md`, `10_2.md`)
- Files contain mathematical formulas using LaTeX notation
- Some chapters include image files for statistical graphs and charts
- Content covers topics like hypothesis testing, probability distributions, statistical inference

## Development Commands

This repository uses Jekyll for static site generation:

```bash
# Serve the site locally (standard Jekyll command)
bundle exec jekyll serve

# Build the site
bundle exec jekyll build
```

## Content Guidelines

- Mathematical notation uses LaTeX syntax within `$$` blocks
- All content is educational and focuses on statistics concepts
- File naming follows pattern: `[chapter]_[section].md` for exercises
- Images are stored alongside markdown files in chapter directories
- Content includes both theoretical explanations and practical problem solutions

## Technical Notes

- **MathJax Version**: Uses MathJax 3 loaded from CDN
- **Markdown Engine**: kramdown with GitHub Flavored Markdown input
- **Math Preview**: Enabled in kramdown configuration
- **Language**: All content and page titles are in Japanese