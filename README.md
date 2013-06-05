Patchwork
=========

## Wtf is this?

Patchwork content management system and blogging platform built on Git and GitHub. It's a loose collection of applications, each meant to handle one piece of content management.

The current collection includes:

* A content repository in GitHub.
* [Thread](https://github.com/joebadmo/patchwork-thread)
* [Quilt](https://github.com/joebadmo/patchwork-quilt)
* [Needle](https://github.com/joebadmo/patchwork-needle)

## Uh... how does it work?

You only really need three pieces: a content repo, Thread, and Quilt. Once you have it set up, Thread reads the content repo, parses the markdown files, and updates a database, an IndexTank API-compatible search index, and uploads specified assets to an Amazon S3 bucket. Quilt then serves the content.

You can also set up a post-receive webhook on the content repo, so whenever you push new content to that repo, the resulting site served by Quilt automatically gets updated.

## Why? Why? Whyyyyyy???

We hate web-based text editors. We like to use our own text editors. We also like Git and GitHub. For a content store, a simple directory structure with markdown files is simple and easy to understand. Storing content in a Git repo also offers the added bonus of version control for your content.

## Why not just use [Jekyll](https://github.com/mojombo/jekyll)?

Jekyll is great! It was one of the inspirations for this project. But there are a few things we don't like about it:

* Static sites are fast and easy to understand, but somewhat inflexible.
* It's not easy to set up on a modern PaaS.
* The content is mixed up with code, configuration, and metadata, which makes collaboration less than straightforward.

## Why all the different pieces?

We were kind of tired of large, monolithic frameworks. We wanted a logical separation of concerns that would allow us to switch out different pieces for different purposes.

## Who do you think you are?

We're [@joebadmo](https://github.com/joebadmo) & [@davidkofahl](https://github.com/davidkofahl). We're learning as we go.

# License

The MIT License (MIT)

Copyright (c) 2013 Joe Moon

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
