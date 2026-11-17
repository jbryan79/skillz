# skillz

Agent Skills by [JABSystems](https://jabsystems.io).

An Agent Skill is a folder with a `SKILL.md` file that teaches an AI agent how to do one kind of task well. The skills here follow the open [Agent Skills](https://agentskills.io) format. This repo is also a Claude plugin marketplace, so each skill installs as a plugin.

## Skills

| Skill | Version | What it does |
| --- | --- | --- |
| [art-from-writing](plugins/art-from-writing/skills/art-from-writing/SKILL.md) | 1.0 | Turns a piece of writing into an original artwork of how it feels. |

## art-from-writing

Share an essay, a letter, a poem, a speech or a set of vows, and say as much or as little as you like about what it did to you. The skill makes one original artwork that carries the feeling. It is not an illustration of the plot, and it is not a decorated quotation.

**When it runs.** When someone shares writing and wants art made from it, says it moved them beyond words, or says "create what you feel" or "make something from this", even with no direction at all.

**What you get.** By default, one self-contained HTML page with a single canvas, plus a still image. The page performs for 30 to 60 seconds and then settles into a resting state that stays quietly alive. You can zoom in until the words are readable, replay it, or skip to the end.

**How it decides.** It makes the choices itself and asks a question only when a wrong guess would be costly. If you give direction, such as a medium, a color or a size, it follows that.

**Whose words go on the piece.** Personal writing that is yours to share, such as a letter, vows or a toast, can become the material of the piece, word for word. Published work by someone else is not reproduced. The art is made from its feeling and imagery instead.

### The method

1. Read it twice, once as a reader and once as a maker.
2. Name the feeling privately, then turn it into temperature, weight, speed and light.
3. Find the form inside the writing: subject, composition, closing gesture, medium.
4. Decide what the words do.
5. Build it.
6. Look at it, and fix what you see.
7. Hand it over with a short note.

The full instructions are in [`SKILL.md`](plugins/art-from-writing/skills/art-from-writing/SKILL.md).

### Example: *While It's Still Hot*

<img src="examples/art-from-writing/while-its-still-hot.jpg" width="440" alt="A cup of coffee seen from above on a saucer. Rings of small dashes circle the saucer and the cup. The milk forms a heart made of nested lines of dashes, with one stroke down its middle. Below it, the title: while it's still hot.">

The method was written down while making this piece. It is a latte seen from above, drawn with all 650 words of an essay in the order they were written. The opening circles the saucer, each step of the essay has its own layer, and the essay's closing words are the single stroke that turns the milk into a heart.

In this image and in the clip, each word is drawn as a mark instead of readable text, so the essay itself stays private.

The pour takes 60 seconds. [Download the clip (MP4, 10 MB)](examples/art-from-writing/while-its-still-hot.mp4); GitHub does not play a file this size in the page.

## Install

### As a plugin

This repo is a Claude plugin marketplace named `skillz`. The plugin is named `art-from-writing`.

**Claude app.** Open **Customize > Plugins**, choose **Add marketplace**, enter `jbryan79/skillz`, then install **Art from Writing**.

**Claude Code.** Run these two commands in your shell. They are the same in bash and PowerShell.

```bash
claude plugin marketplace add jbryan79/skillz
claude plugin install art-from-writing@skillz
```

### As a single skill

The skill folder is `plugins/art-from-writing/skills/art-from-writing`.

**Claude app.**

1. Download that folder and zip it, so that the folder itself is the top level of the ZIP.
2. Open **Customize > Skills** and upload the ZIP as a new skill.
3. Make sure code execution is turned on. Skills need it.

Claude's help center has the current steps: [Use skills in Claude](https://support.claude.com/en/articles/12512180).

**Claude Code.** Copy that folder into your personal skills folder:

- macOS and Linux: `~/.claude/skills/`
- Windows: `C:\Users\<you>\.claude\skills\`

### Try it

Share a piece of writing and say "create what you feel."

## What's in this repo

```
skillz/
├── .claude-plugin/
│   └── marketplace.json        lists the plugins in this repo
├── plugins/
│   └── art-from-writing/       the plugin
│       ├── .claude-plugin/
│       │   └── plugin.json
│       ├── assets/
│       │   └── icon.png        the plugin's icon
│       ├── README.md
│       └── skills/
│           └── art-from-writing/
│               ├── SKILL.md    the skill
│               └── LICENSE.txt MIT license, so it travels with the skill
├── examples/
│   ├── README.md               license note for the example artwork
│   └── art-from-writing/
│       ├── while-its-still-hot.jpg
│       └── while-its-still-hot.mp4
├── LICENSE
└── README.md
```

## Credit

Created by [JABSystems](https://jabsystems.io) with Claude, November 2026.

## License

The skills, the plugin and this README are released under the [MIT License](LICENSE), copyright 2026 JABSystems.

The example artwork in [`examples/`](examples/) and the plugin's icon, which is a detail of the same piece, are not covered by that license. All rights reserved.
