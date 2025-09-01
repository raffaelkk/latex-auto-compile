# LaTeX Auto-Compile Repository

This repository automatically compiles ALL `.tex` files to PDF using GitHub Actions.

## How it works

1. **Add your `.tex` files anywhere** in the repository (recommended: use the `input/` directory)
2. **Push to GitHub** - the workflow triggers automatically
3. **Download compiled PDFs** from the Actions tab as artifacts

## Features

- ✅ Automatically finds and compiles ALL `.tex` files in the repository
- ✅ Preserves directory structure in output
- ✅ Continues compilation even if some files fail
- ✅ Uses latexmk for proper dependency resolution
- ✅ Non-interactive mode to handle errors gracefully

## Directory Structure

```
├── input/          # Place your .tex source files here
├── out/            # Compiled PDFs (created by GitHub Actions)
└── .github/
    └── workflows/
        └── compile-latex.yml  # Automated compilation workflow
```

## Usage

Simply push any `.tex` file to this repository and it will be automatically compiled to PDF!

```bash
# Add your LaTeX file
cp your-document.tex input/

# Commit and push
git add input/your-document.tex
git commit -m "Add new document"
git push
```

## View Results

1. Go to the [Actions tab](../../actions) on GitHub
2. Click on the latest workflow run
3. Download the `all-compiled-documents` artifact
4. Extract to find all compiled PDFs