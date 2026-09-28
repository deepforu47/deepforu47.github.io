---
layout: post
title: "Welcome to My New Blog"
date: 2026-09-28 16:00:00 +0100
author: Kuldeep Sharma
tags: [welcome, tech, jekyll, ai]
---

Welcome to my new personal blog hosted on GitHub Pages!

I set up this blog to share technical guides, thoughts on software craftsmanship, and deep dives into the rapidly evolving world of Artificial Intelligence.

### What to Expect

Here is a glimpse of the topics I will be covering:

1. **AI & Machine Learning**: Insights into agentic workflows, large language models, neural network architectures, and practical hands-on tutorials.
2. **Software Craftsmanship**: System design principles, clean architecture patterns, performance tuning, and idiomatic code design.
3. **Developer Productivity & Tooling**: Exploring modern developer tools, CLI utilities, and open-source ecosystems.

### Code Highlighting in Jekyll

Jekyll comes with first-class support for syntax highlighting via Rouge. Here is a simple Python snippet:

```python
from dataclasses import dataclass

@dataclass
class Post:
    title: str
    author: str
    tags: list[str]

    def display(self) -> str:
        tags_formatted = " ".join(f"#{t}" for t in self.tags)
        return f"{self.title} by {self.author} | {tags_formatted}"

if __name__ == "__main__":
    post = Post(
        title="Welcome to My New Blog",
        author="Kuldeep Sharma",
        tags=["welcome", "tech", "jekyll", "ai"]
    )
    print(post.display())
```

### Stay in Touch

Feel free to browse around, check out the [Archive](/archive/) to see past articles, or head over to the [About](/about/) page to learn more about my background. You can also subscribe to the [RSS Feed](/feed.xml) to get notified whenever a new post goes live.

Thanks for visiting, and stay tuned for upcoming articles!
