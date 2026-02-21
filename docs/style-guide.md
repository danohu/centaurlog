# Centaurlog Style Guide

Guidelines for writing content on this blog.

## Voice and Perspective

**Default voice: "we"**
- Use "we" for collaborative work between Dan and Claude
- Example: "We set up the repository structure..."
- Example: "We explored several approaches..."

**Specify when relevant:**
- Use "Claude" when referring to AI-specific actions or capabilities
  - Example: "Claude generated the initial layout templates..."
- Use "Dan" when referring to human-specific decisions or guidance
  - Example: "Dan chose the blog name Centaurlog..."

**Avoid:**
- Excessive "I" statements (ambiguous who "I" is)
- "The AI" or "the LLM" (too impersonal when we have a name)

## Attribution and Transparency

**On every post:**
- Include `model` field in frontmatter (e.g., "Claude Sonnet 4.5")
- Trust the site-wide attribution in header/footer
- Don't repeat "this was written by AI" in every post body

**When discussing AI:**
- Be matter-of-fact, not apologetic
- Focus on what was done, not disclaimers
- Example: "We used Claude's ability to..." not "I'm just an AI but..."

## Tone

**Professional but conversational:**
- Technical accuracy is important
- Avoid overly formal academic writing
- Use examples and concrete details
- It's okay to be opinionated

**Honest about limitations:**
- Acknowledge when we don't know something
- Note when approaches are experimental
- Share what didn't work, not just successes

## Content Types

**Technical posts:**
- Clear problem/solution structure
- Code examples with explanations
- Links to references and further reading

**Process posts:**
- Document workflows and decisions
- Share lessons learned
- Include both successes and challenges

**Reference posts:**
- Designed for future lookup
- Clear headings and structure
- Concrete examples

## Formatting

**Headings:**
- H1 for post title only (handled by layout)
- H2 for main sections
- H3 for subsections

**Code blocks:**
- Always specify language for syntax highlighting
- Include context about what the code does
- Show relevant output when helpful

**Links:**
- Link to sources and references
- Use descriptive link text (not "click here")
- External links open in same tab (this is a blog, not a web app)

## Metadata

**Required frontmatter:**
```yaml
---
layout: post
title: "Descriptive Title"
date: YYYY-MM-DD
model: "Claude Sonnet 4.5"
---
```

**Optional frontmatter:**
```yaml
tags: [tag1, tag2]  # Keep to 2-4 relevant tags
excerpt: "Brief summary for index page"
```

## Topics

**In scope:**
- Technical tutorials and guides
- Process documentation and workflows
- AI/LLM collaboration insights
- Software development practices
- Research summaries and explanations

**Out of scope (for now):**
- Personal diary-style posts
- Opinion pieces without technical substance
- Content that should live in project-specific docs

## Audience

**Primary:** Dan (future reference)
- Assume technical background
- Can reference past context
- Focus on usefulness over completeness

**Secondary:** People Dan shares URLs with
- Provide enough context to understand standalone
- Link to related posts for deeper background
- Assume general technical literacy

## Examples

**Good opening:**
> We recently converted the OED project to use git worktrees, which solved the problem of managing multiple parallel feature branches without constant context switching.

**Less good opening:**
> As an AI language model, I helped set up git worktrees. This post, which was written by Claude Sonnet 4.5, will explain how we did this.

---

**This guide will evolve as we learn what works.**
