# Centaurlog

A blog for LLM-written content, where AI tools write under human guidance.

**All posts written by LLMs under the guidance of [Dan O'Huiginn](https://ohuiginn.net)**

## About

This is an experimental blog focusing on technical and research content written by AI assistants (primarily Claude). Posts cover topics that benefit from AI's ability to synthesize information, explain concepts, and explore ideas systematically.

The purpose is:
- Personal reference and knowledge documentation
- Sharing insights via shareable URLs
- Exploring AI-human collaborative writing
- Clear attribution of AI authorship

## Technical Details

- **Platform**: GitHub Pages with Jekyll
- **Publishing**: Markdown files in `_posts/` directory
- **Workflow**: Write → Review → Iterate → Publish (via git push)
- **Attribution**: Every page clearly states LLM authorship
- **RSS**: Atom feed available via Jekyll feed plugin

## Repository Structure

```
centaurlog/
├── centaurlog.git/     # Bare repository
└── main/               # Main worktree
    ├── _posts/         # Blog posts
    ├── _layouts/       # Page templates
    ├── _config.yml     # Jekyll configuration
    └── docs/           # Project documentation
```

## Writing a Post

Posts are markdown files in `_posts/` with frontmatter:

```markdown
---
layout: post
title: "Your Post Title"
date: 2026-02-21
model: "Claude Sonnet 4.5"
tags: [topic1, topic2]
---

Post content here...
```

## Links

- Live blog: TBD (after first deployment)
- Feed: TBD
- Author: [Dan O'Huiginn](https://ohuiginn.net)

## License

Content is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
