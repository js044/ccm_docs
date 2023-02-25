# Hugo

Hugo is the static site generator we use to create and maintain Cicada. This page is most useful for Web Developers.

## Install 

Please visit Hugo Docs to get started with installation. You can find instructions for Windows, Mac, Linux, and BSD [here](https://gohugo.io/installation/). Work with our current Web Developer to get access to CCM's repository and then you will be ready to modify the site.


## Publishing an issue

To publish an issue, the Web Devloper must first create the issue. Our "issues" file tree broadly looks like this.

```
├── content
│   ├── issues
│   │   ├── issue-1
│   │   │   ├── art
│   │   │   │   └── art-piece-1.md
│   │   │   └── writing
│   │   │   │   └── writing-piece-1.md
│   │   │   └── _index.md
│   │   ├── issue-2
│   │   │   ├── art
│   │   │   │   └── art-piece-1.md
│   │   │   └── writing
│   │   │   │   └── writing-piece-1.md
│   │   │   └── _index.md
│   │   ├── ...
│   └── _index.md
```

With this in mind:

1. Create the folder for whatever issue we're working on.
2. Create an _index.md page using ```hugo new content/issues/issue-[#]/_index.md```
3. The following front matter should generate based on the ```archetypes``` folder. 

```
---
title: 
draft: false
date: 
featuredImage: 
summary:
---
```
5. Check previous issues for pointers on how to fill out the featuredImage (cover) and summary. 
6. Make an art and writing folder within the issue folder following the naming convention laid out in the content tree.
7. After this, you can create webpages for different pieces. Our issue pages work by rendering different types of content in different ways--we use a mix of thumbnails and text titles. For this to work, we have to add front matter to each piece clarifying its type, which you can do using the following command template:

`hugo new -k [writing/art] issues/issue-[#]/[writing/art]/[title.md]`

The `-k` denotes type of thumbnail. 

**Example**: `hugo new -k writing issues/issue-2/writing/writing-piece-1.md` would create a webpage that goes to /issue-2/writing-piece-1 

**Note**: Our config file allows us to skip the writing/art slug when the page is loaded. (Why it renders as /issue-2/writing-piece-1 instead of /issue-2/writing/writing-piece-1)

```
  [permalinks]
  issues = "/:sections[1:]/:title"
```

8. The actual content of the pieces will vary. Some will be simple, some will require more involved coding. For example, some poetry may require HTML instead of simple Markdown. 
    - Visual art pieces are uploaded with the following format: ```<a href = "/images/issue[#]/name.jpg" data-lightbox="img">![image](/images/issue[#]/name.jpg#issues)</a>```
9. You set the order of the post in the front matter with `weight`. It is recommended to upload pieces in sequential order to make it easier to number the posts.
10. Be sure to update the `issues.html` and `landing.html` pages with the new issue before announcing!


## Making a blog post

1. Creating a blog post is a lot more straightforward:
    
    `hugo new content/blog/[title.md]`

2. Fill out the front matter and blog post. Check previous blog posts for a better idea of how to best manage them. There are specific folders for blog images. Make sure you're saving images in a logical place and referencing them correctly.

