# Markdown Meeting Notes → Google Doc (Google Colab)

## Description
A Python tool that converts markdown meeting notes into a well-formatted Google Doc using the Google Docs API.
It supports headings (H1/H2/H3), nested bullet indentation, markdown checkboxes as Google Docs checkboxes,
distinct styling for @mentions, and footer styling.

## Features
- Creates a new Google Doc programmatically
- Markdown headings:
  - Title → Heading 1
  - Sections → Heading 2
  - Sub-sections → Heading 3
- Nested bullet hierarchy with indentation
- `- [ ]` markdown checkboxes → Google Docs checkboxes
- Styles `@mentions` (bold + color)
- Footer section styled differently (italic + small + gray)

## Dependencies
- google-api-python-client
- google-auth
- google-auth-httplib2
- google-auth-oauthlib

## Setup / Run in Google Colab
1. Open the notebook: `notebook/markdown_to_gdoc.ipynb`
2. Run the install cell:
   ```bash
   !pip -q install google-api-python-client google-auth google-auth-httplib2 google-auth-oauthlib
