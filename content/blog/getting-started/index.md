---
title: Global `.gitignore` for all
subtitle: Tired of creating a `.gitignore` file for each project? Discover a more efficient approach; a global .gitignore file that works across all your projects!

# Summary for listings and search engines
summary: Tired of creating a `.gitignore` file for each project? Discover a more efficient approach; a global .gitignore file that works across all your projects!

# Link this post with a project
projects: []

# Date published
date: '2023-10-19T00:00:00Z'

# Date updated
lastmod: '2023-10-19T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Version control

categories:
  - Tips
---

According to the Git documentation, Git uses various sources to find patterns for files to ignore, including the familiar project-specific `.gitignore` file and patterns specified in the `core.excludesFile` configuration variable.

# Setting Up the Global .gitignore

Let's establish the global .gitignore file. Git sources ignore patterns from various places, including project-specific `.gitignore` files and patterns from the `core.excludesFile` configuration variable.

> 📝 Note that the local `.gitingore` file will always be more prioritized than the global one. (i.e. if a file is ignored in the global .gitignore file, but explicitly tracked in the local .gitignore file, it will be tracked, and vice versa)

## Step 1: Create the Global `.gitignore`

Start by creating a global `.gitignore` file in your home directory with the name `.gitignore_global`:

```shell
touch ~/.gitignore_global
```

## Step 2: Adding Patterns to Ignore
Next, add patterns to this global `.gitignore` file. For instance, to ignore all log files, use the following command:

```shell
echo "*.log" >> ~/.gitignore_global
```
You can include as many patterns as you need.

## Step 3: Configuring Git

To make Git use your global .gitignore, you need to set the core.excludesFile configuration variable. Run the following command:

```python
git config --global core.excludesfile ~/.gitignore_global
```
And there you have it! You now have a global .gitignore that Git will use across all your projects.


## Bonus Tip: Pre-made global `.gitignore`
You can find pre-made global `.gitignore` files for various programming languages and tools at [gitignore.io](https://www.toptal.com/developers/gitignore).

