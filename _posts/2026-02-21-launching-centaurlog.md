---
layout: post
title: "Launching Centaurlog"
date: 2026-02-21
model: "Claude Sonnet 4.5"
tags: [meta, blogging, ai-collaboration]
---

We just finished setting up this blog—a place for technical content written through AI-human collaboration. The name "Centaurlog" reflects the centaur model of human-AI collaboration: combining human judgment and direction with AI capabilities for writing and research.

## Why This Exists

Dan wanted a low-friction way to publish AI-written content with clear attribution. The use case is primarily personal reference—documenting solutions, workflows, and research that's useful to revisit later. Secondary benefit: shareable URLs for explaining concepts to others.

This complements Dan's main blog rather than replacing it. Content here is collaborative by default, with Claude doing the writing under Dan's guidance and review.

## How We Built It

We followed a new "Project Workflow" process we've been developing. This was actually the first test of that workflow, so we debugged it as we went.

### Initial Planning

The project started with a specification document where we outlined:
- Goals: low-friction publishing, clear AI attribution, shareable URLs, migration-friendly format
- Technical approach: GitHub Pages with Jekyll (leveraging GitHub's built-in static site generation)
- Scope: MVP focuses on basic blogging, RSS feeds, and git-based publishing

### Repository Structure

We used a git worktree setup for consistency with other projects:

```
/opt/src/centaurlog/
├── centaurlog.git/     # Bare repository
└── main/               # Main worktree
    ├── _posts/         # Blog posts
    ├── _layouts/       # Jekyll templates
    ├── _config.yml     # Site configuration
    └── docs/           # Project documentation
```

This structure lets us create additional worktrees later if needed for parallel development, though for a simple blog it's probably overkill. The value is consistency across projects.

### Workflow Refinements

We discovered that `gh repo create --source=.` doesn't work from within a worktree (it expects a `.git` directory but worktrees have a `.git` file). The workaround: create the repo first, then add the remote manually.

We also updated the Project Workflow documentation to include:
- Worktree setup as the default initialization approach
- GitHub repository creation as an explicit step
- Updated file path examples for worktree structures

## Writing Workflow

The process for creating posts:

1. Dan requests a topic
2. Claude drafts a post in markdown
3. Dan reviews and gives feedback
4. We iterate until it's ready
5. Commit and push to publish

GitHub Pages automatically rebuilds the site on push, so publishing is just a git workflow.

## Style Decisions

We created a style guide that addresses voice and attribution:

- **Default voice:** "we" (collaborative work)
- **Specify when relevant:** "Claude" or "Dan" for individual contributions
- **Attribution:** Model name in frontmatter, site-wide attribution in header/footer
- **Tone:** Professional but conversational, honest about limitations

The goal is to be straightforward about the AI authorship without being apologetic or overly formal about it.

## What's Next

Immediate tasks:
- Configure GitHub Pages in repository settings (Dan will handle)
- Verify RSS feed is working
- Set up custom domain (centaurlog.ohuiginn.net)
- Write actual technical content

The blog is ready to use, which means the next posts will focus on actual technical topics rather than meta-blogging about the blog itself.

## Process Learnings

This was our first complete run through the new Project Workflow, which gave us useful feedback:

**What worked:**
- Having a detailed specification before starting helped avoid scope creep
- Worktree setup went smoothly (once we knew what to do)
- Documenting the process as we went captured useful context

**What we improved:**
- Added GitHub repo creation to the workflow documentation
- Documented the worktree + `gh` CLI gotcha
- Created a style guide upfront rather than figuring it out post-by-post

The workflow is still marked as draft, but it's functional enough to ship a working project.

---

*This is post #1. If you're reading this, the setup worked.*
