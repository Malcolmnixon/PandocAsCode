# File Layout

Each document should have its own source folder in the source repository, containing the following files:

 - `<document>.yaml` containing the document settings
 - `title.txt` containing the document title information
 - `xx-<section>.md` containing the sections of the document
 - `assets/xx.yy` document assets such as images


## Document Settings

The `<document>.yaml` file should contain the following:

```
input-files:
- ${.}/title.txt
- ${.}/xx-<section>.md
- ${.}/xx-<section>.md
- ${.}/xx-<section>.md

table-of-contents: true

number-sections: true

resource-path:
- ${.}
- ${.}/assets
```


## Title File

The `title.txt` file should contain the following:

```
---
title: Pandoc-as-Code
author: Malcolm Nixon
rights:  Creative Commons 1.0 Universal (CC0 1.0)
language: en-US
...
```


## Section Markdown Files

The `xx-<section>.md` files should contain the following:

```
# Section Heading

Section text using markdown syntax
```


## Image Files

The section markdown files can contain image references such as:

```
![Image Title](<image-path>)
```

For example:
```
![CC0 Logo](assets/cc-zero.png)
![CC0 Logo](assets/cc-zero.png){ width=100px }
```

Produces:

![CC0 Logo](assets/cc-zero.png)
![CC0 Logo](assets/cc-zero.png){ width=100px }
