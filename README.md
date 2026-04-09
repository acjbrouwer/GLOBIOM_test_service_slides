# The GLOBIOM test service

## Abstract

This seminar details the purpose, history, function, and use of the GLOBIOM test service available to GLOBIOM core team members at https://jenkins.iiasa.ac.at. The service is scalable, supports reproducible clean-slate tests, and features special provisions for GLOBIOM testing.

## About GLOBIOM

GLOBIOM is an IIASA model. See https://globiom.org.

## About the Test Service

The test service is a Jenkins instance deployed on Kubernetes.

## Repository Purpose

This repository contains Markdown slides for the presentation, which can be converted to PPTX or other formats using Pandoc.

**Note:** This README.md and the slides will be updated incrementally.

## Slide Development Workflow

### Prerequisites

- Install Pandoc: Follow instructions at https://pandoc.org/installing.html (e.g., via package manager: `apt install pandoc` on Ubuntu, `brew install pandoc` on macOS).

### Elaborating Slides in Markdown

- Create slide files with `.md` extension (e.g., `slides.md`).
- Use level 1 headers (`# Slide Title`) to start new slides. Pandoc treats each level 1 header as a new slide by default.
- Write content using standard Markdown syntax:
  - Paragraphs
  - **Bold** and *italic* text
  - Bullet points and numbered lists
  - Links: `[text](url)`
  - Images: `![alt text](image.png)`
  - Code blocks: ```language\ncode\n```
- Optionally, use horizontal rules (`---`) to force slide breaks between content.
- Add metadata at the top of the Markdown file for title, author, etc.:

  ```
  ---
  title: The GLOBIOM test service
  author: Your Name
  date: YYYY-MM-DD
  ---
  ```

- For advanced formatting, refer to Pandoc's Markdown extensions: https://pandoc.org/MANUAL.html#pandocs-markdown

### Generating PPTX

To convert the Markdown file to a PowerPoint presentation:

```bash
pandoc slides.md -t pptx -o slides.pptx
```

This uses Pandoc's default PowerPoint template. For custom themes, use the `--reference-doc` option with a reference PPTX file.

### Generating LibreOffice Impress File

To generate an OpenDocument Presentation (ODP) file, which can be opened and edited in LibreOffice Impress:

```bash
pandoc slides.md -t odp -o slides.odp
```

ODP files are compatible with LibreOffice and other OpenDocument-supporting applications.
