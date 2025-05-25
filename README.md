![PyPI](https://img.shields.io/pypi/v/mkdocs-with-confluence)
[![Build Status](https://app.travis-ci.com/pawelsikora/mkdocs-with-confluence.svg?token=Nxwjs6L2kEPqZeJARZzo&branch=main)](https://app.travis-ci.com/pawelsikora/mkdocs-with-confluence)
[![codecov](https://codecov.io/gh/pawelsikora/mkdocs-with-confluence/branch/master/graph/badge.svg)](https://codecov.io/gh/pawelsikora/mkdocs-with-confluence)
![PyPI - Downloads](https://img.shields.io/pypi/dm/mkdocs-with-confluence)
![GitHub contributors](https://img.shields.io/github/contributors/pawelsikora/mkdocs-with-confluence)
![PyPI - License](https://img.shields.io/pypi/l/mkdocs-with-confluence)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/mkdocs-with-confluence)

### Requirements

- md2cf
- mimetypes
- mistune

# Installation

This project uses MkDocs to generate documentation locally and integrates with Atlassian Confluence to automatically publish pages.

Installation

Step - 1

Clone the repository,

git clone https://github.com/denizzsarierr/mkdocs-with-confluence
cd mkdocs-with-confluence

Step - 2

Create and activate a virtual environment,

python -m venv .venv

# PowerShell

venv\Scripts\activate

# macOS/Linux

source .venv/bin/activate

Step - 3

Install required modules,

- pip install --upgrade pip (If not up to date)
- pip install mkdocs-with-confluence
- pip install -r requirements.txt

Step - 4

Set environment variable for Confluence publishing,

# PowerShell

- $env:MKDOCS_TO_CONFLUENCE = "1"

# macOS/Linux

- export MKDOCS_TO_CONFLUENCE=1

Step - 5

# Usage

Local host,

mkdocs serve

- Opens a development server at http://127.0.0.1:8000/. (Expected output)

Step - 6

Build static site:,

mkdocs build

Generates the site/ folder with static HTML files.

Step - 7

Publish to Confluence:,

mkdocs build -v

Publishes or updates pages under the configured parent in Confluence.

Configuration,
Edit mkdocs.yml to set your Confluence credentials and parent page:

Step - 8

plugins:

- search
- mkdocs-with-confluence:
  host_url: 'https://your-username-domain.atlassian.net/wiki/rest/api/content'
  space: '<SPACE_KEY>'
  parent_page_name: ''
  username: 'outlinecodetr@gmail.com'
  api_token: '<API_TOKEN>'

# License

MIT © denizzsarierr
