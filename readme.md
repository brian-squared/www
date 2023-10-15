This repository generates our blog.

# Writing a new post

1. Create a directory for the blog post, under: `content/posts/<year>/<month>/<name>`
  - Name should be something short and descriptive, but doesn't need to b   e the title of the post
2. Create a file `content/posts/<year>/<month>/<name>/index.md`. It MUST be called `index.md`
3. Write the post in `index.md`. It needs to have a section at the start with the post's metadata (title, date, author, tags):

````
---
title: "This is the post title!"
date: 2023-10-15T10:05:31+01:00
author: "Brian Who?"
tags: ["Pi Wars 2024"]
description: "A subtitle which will show under the title"
---

## Normal markdown syntax

This is the syntax for highlighted python code:

```python
import sys

print(f"This is some example python code: {sys.argv=}")
```

You can use relative paths for images, so this one is in `content/posts/<year>/<month>/<name>/images`:

![Brian² Logo](images/logo.png)

This is the syntax for embedding a tweet:

{{< tweet user="CannonFodder" id="1710628263830098268" >}}
````

# Publishing posts

When you push to the `main` branch, the blog is automatically re-generated,
and will be published at
[https://brian-squared.github.io/www/](https://brian-squared.github.io/www/)
