---
title: Introduction
sidebar_position: 1
---

# Introduction

Docusaurus is a **static-site generator**. It builds a **single-page application** with fast client-side navigation, leveraging the full power of **React** to make your site interactive. It provides out-of-the-box **documentation features** but can be used to create **any kind of site** (personal website, product, blog, marketing landing pages, etc).

## Other tools to create a static website. (Static site generators tools)

- **GatsBy** – Great for performance (but has a learning curve).
- **NextJs** - If we want more than just documentation and need dynamic features. Nextra is an opinionated static site generator built on top of Next.js. It is currently less featured than Docusaurus.
- **VitePress** – Best for Vue JS projects
- **MkDocs** - MkDocs is a popular Python static site generator with value propositions similar to Docusaurus.
- **Docsify** - Docsify makes it easy to create a documentation website but is not a static-site generator and is not SEO friendly.
- **GitBook** - Currently, GitBook is only free for open-source and non-profit teams. Docusaurus is free for everyone.
- **Jekyll** - Popular for GitHub Pages

## Why Docusaurus?

- Built with React, so it's great for React projects.
- MDX support (Markdown + JSX) allows embedding React components.
- Easy to deploy (GitHub Pages, Vercel, Netlify, Azure).
- Out-of-the-box features like versioning, search, and dark mode.
- Pluggable (e.g., Algolia for search).

## Getting Started

Get started by **creating a new site**.

Or **try Docusaurus immediately** with **[docusaurus.new](https://docusaurus.new)**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 18.0 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.

## Generate a new site

Generate a new Docusaurus site using the **classic template**.

The classic template will automatically be added to your project after you run the command:

```bash
npm init docusaurus@latest my-website classic
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

The command also installs all necessary dependencies you need to run Docusaurus.

## Start your site

Run the development server:

```bash
cd my-website
npm run start
```

The `cd` command changes the directory you're working with. In order to work with your newly created Docusaurus site, you'll need to navigate the terminal there.

The `npm run start` command builds your website locally and serves it through a development server, ready for you to view at http://localhost:3000/.

Open `docs/intro.md` (this page) and edit some lines: the site **reloads automatically** and displays your changes.

## Understanding the folder structure

```bash
my-website
├── blog
│ ├── 2019-05-28-hola.md
│ ├── 2019-05-29-hello-world.md
│ └── 2020-05-30-welcome.md
├── docs
│ ├── doc1.md
│ ├── doc2.md
│ ├── doc3.md
│ └── mdx.md
├── src
│ ├── css
│ │ └── custom.css
│ └── pages
│ ├── styles.module.css
│ └── index.js
├── static
│ └── img
├── docusaurus.config.js
├── package.json
├── README.md
├── sidebars.js
```

A standard Docusaurus project includes the following directories:

- **/docs/**: Contains Markdown files for your documentation.
- **/blog/**: Holds Markdown or MDX files for blog posts.
- **/src/**: Includes non-documentation files like pages or custom React components.
- **/src/pages/**: Any JSX/TSX/MDX file here will be converted into a website page.
- **/static/**: For static assets like images and fonts.
- **docusaurus.config.js**: The main configuration file for your site.
- **sidebars.js**: Manages the structure of the sidebar in your documentation.

```

```
