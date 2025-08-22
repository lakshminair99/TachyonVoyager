# TachyonVoyager

A Hugo static site using the Ananke theme.

## Setup

### Initial Clone

```bash
# Clone
git clone https://github.com/lakshminair99/TachyonVoyager.git
```

### First time -- init submodule (theme)

```bash
cd TachyonVoyager
git submodule update --init themes/ananke
```


### Later -- Update theme (do this sometimes)
```
git submodule update --remote themes/ananke
```


## Creating New Posts

### Using Hugo's archetype

```bash
# Create a new post in the appropriate category
hugo new content/posts/Psychology/your-post-title.md
hugo new content/posts/Travel/your-post-title.md
hugo new content/posts/Short_stories/your-post-title.md
```

### Manual creation

Create a new `.md` file in the appropriate category folder under `content/posts/` with front matter:

```yaml
---
title: "Your Post Title"
date: 2025-01-01T00:00:00Z
draft: false
---

Your content here...
```

### Workflow for adding posts

```bash
# 1. Create your new post
hugo new content/posts/Psychology/new-post.md

# 2. Edit the post content
# Edit the file in your preferred editor

# 3. Test locally
hugo server -D

# 4. Commit directly to main
git add .
git commit -m "Add new post: your post title"
git push origin main
```

## Development

```bash
# Start Hugo development server
hugo server -D
```

## Building

```bash
# Build static site
hugo
```

## Notes

- Always use `--recurse-submodules` when cloning
- Always use `--recurse-submodules` when pulling if you want latest submodule changes
- Check `git submodule status` before committing if you've updated themes
