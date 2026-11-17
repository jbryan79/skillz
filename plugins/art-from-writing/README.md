# Art from Writing

Turn a piece of writing into an original artwork of how it feels.

Share an essay, a letter, a poem, a speech or a set of vows, and say as much or as little as you like about what it did to you. Claude makes one original artwork that carries the feeling. By default that is a single web page that performs for under a minute and then rests, plus a still image. It is not an illustration of the plot, and it is not a decorated quotation.

## Install

Inside a Claude Code session, version 2.1.275 or later, type:

```
/plugin install art-from-writing --marketplace jbryan79/skillz
```

In the Claude app, open **Customize > Plugins**, choose **Add marketplace**, enter `jbryan79/skillz`, and install **Art from Writing**.

## How to use it

Share the writing and say "create what you feel" or "make something from this." No direction is needed. If you give some, such as a medium, a color or a size, the skill follows it.

## What is inside

One skill, `art-from-writing`. It is a set of written instructions with seven steps:

1. Read it twice.
2. Name the feeling privately.
3. Find the form inside the writing.
4. Decide what the words do.
5. Build it.
6. Look at it.
7. Hand it over.

## What it runs and sends

- The plugin has no hooks, no connectors, no executables and no settings. It sends nothing anywhere.
- The artwork is one self-contained page that makes no network requests. Where Claude has artifact tools, the page is published as a private artifact in your own account. Otherwise it is delivered as a file.
- To check its work, the skill has Claude open that page in a local headless browser when one is available.
- Personal writing that is yours to share can be used word for word as the material of the piece. Published work by someone else is not reproduced.

## Credit and license

Created by JABSystems with Claude, November 2026.

MIT License. The full terms are in `skills/art-from-writing/LICENSE.txt`.

The icon is a detail of *While It's Still Hot*, the piece this method was written down from. The icon is not covered by the MIT license. All rights reserved.

Source and an example piece: https://github.com/jbryan79/skillz
