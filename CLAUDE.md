# Centaurlog

A blog for LLM-written content with clear AI authorship disclosure.

## Project Context
- **Purpose**: Low-friction publishing platform for AI-written technical/research content
- **Location**: /opt/src/centaurlog/main/
- **Platform**: GitHub Pages with Jekyll
- **Attribution**: All posts written by LLMs under guidance of Dan O'Huiginn
- See docs/spec.md for detailed specification

## Structure
- Worktree setup: bare repo at `../centaurlog.git/`, main worktree at `main/`
- `local/` directory for per-worktree state (currently unused, reserved for future use)

## Workflow

### Writing and Publishing Posts
1. User requests post topic
2. Write markdown draft in `_posts/` with naming: `YYYY-MM-DD-title.md`
3. User reviews and provides feedback
4. Iterate until satisfied
5. Commit and push to publish

### Post Format
Posts use Jekyll frontmatter:
```yaml
---
layout: post
title: "Post Title"
date: YYYY-MM-DD
model: "Claude Sonnet 4.5"
tags: [tag1, tag2]
---
```

### Git Workflow
- Single-user repo: commit and push to main branch
- Standard commit message format with AI co-author attribution

## Dependencies
- GitHub Pages (Jekyll auto-builds on push)
- Jekyll theme adapted from danohu.github.io
- No local Jekyll installation needed (GitHub builds)

## Quick Commands

```bash
# Create new post
touch _posts/$(date +%Y-%m-%d)-post-title.md

# Commit and publish
git add _posts/YYYY-MM-DD-post-title.md
git commit -m "Add post: Title"
git push origin main

# List worktrees
git worktree list
```
