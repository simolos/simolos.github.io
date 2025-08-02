# Simona Losacco personal site

Contents:
- [Site template](#site-template)
- [Editing guide](#editing-guide)
- [Local development](#local-development)

## Site template

This lightweight site is based on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template
for personal and professional portfolio-oriented websites.

This repo uses [Jekyll](https://jekyllrb.com/docs/), a static site generator that takes text written in standard favorite markup
language and uses layouts to create a static website. This means you can easily write and maintain site content with any text editor
and get a clean and consistent style without any HTML or CSS.

## Editing guide

Refer to https://academicpages.github.io/ for an introduction to the site template.

Additionally, see https://academicpages.github.io/markdown for a guide on how to manage files, markdown documents, equations,
diagrams and plots to create and manage your site content.

The [Jekyll documentation](https://jekyllrb.com/docs/pages/) also describes the specifics of pages, posts, collections and
so on in more detail.

The following sections here are less detailed but should serve as a convenient local reference:

### Configuration

The [_config.yml](./_config.yml) file defines site-wide configurations and the sidebar content.
This can mainly be used to set author profile details, but also allow deeper customization of page defaults and categories.

### Navigation

The navbar at the top is defined by [_data/navigation.yml](./_data/navigation.yml). Add, re-order or remove navigation links.

### Pages

The [_pages](./_pages) directory holds top-level site content as markdown (.md) files, or HTML if you're feeling fancy.

The landing page is defined in [_pages/about.md](./_pages/about.md). A new page can be added by making a new markdown file,
adding [frontmatter](#page-metadata), and then linking to the page in the navbar or from another page.

Other "category" pages such as [_pages/publications.html](./_pages/publications.html) or [_pages/talks.html](./_pages/talks.html)
use some code to group pages in [collections](#collections).

#### Page metadata

Markdown pages start with "frontmatter" in the following format:

```markdown
---
permalink: /markdown/
title: "Markdown"
author_profile: true
redirect_from:
  - /md/
  - /markdown.html
---
```

The `permalink` defines the URL of the page, relative to the root of the site. The link name can be anything, but it is useful to keep it to the same name as the file. Then, this link can be used in the [navbar](#navigation) or from other pages.

Naturally, `title` determines the title text shown at the top of the page.

If `author_profile` is set to false, then the left profile section is hidden on this page.

Finally, `redirect_from` defines additional proxy links that redirect to this page.

#### Collections

This template includes blog posts, talks, publications and more as collections of pages in a category.
The actual content within a collection is grouped by subfolders (for examples, [_publications](./_publications) or [_talks](./_talks))
and then is rendered automatically. This means adding new content to a collection is easy and requires no changes to the
top-level category page.

The pages within these subfolders have extra metadata in the frontmatter (for example, `collection: talks`) to link them to that collection.

There is some additional metadata in [_config.yml](./_config.yml) that defines default settings and paths for collections.

### Assets (files and images)

Add files to the [files](./files) folder, and add images to the [images](./images) folder.

To show an image on a page, format a link with `![reference](url)`, where reference is some .

```markdown
![profile](/images/profile.png)
```

## Local development

When you are initially working on your website, it is very useful to be able to preview the changes locally before pushing them to GitHub.

### Running locally with Docker

Make sure you have [Docker](https://www.docker.com/) installed and running.

You can then build and execute the container by running the following command in the repository:

```bash
docker compose up
```

You should now be able to access the website in the browser from `localhost:4000`.

Any changes you make and save to page content will be automatically reloaded in the browser.
However, some configurations such as major changes to the `_config.yml` file may require restarting the Docker container.
This can be done using CTRL+C to terminate the running container followed by re-entering the previous command.

### Using the DevContainer in VS Code

If you are using [Visual Studio Code](https://code.visualstudio.com/) you can use the [Dev Container](https://code.visualstudio.com/docs/devcontainers/containers) that comes with this Repository. Normally VS Code detects that a development coontainer configuration is available and asks you if you want to use the container. If this doesn't happen you can manually start the container by **F1->DevContainer: Reopen in Container**. This restarts your VS Code in the container and automatically hosts your academic page locally on http://localhost:4000. All changes will be updated live to that page after a few seconds.
