---
name: art-from-writing
description: "Turn a piece of writing into an original artwork of how it feels - a living page that performs and then rests, plus a still. Use whenever someone shares an essay, letter, poem, speech, vows or message and wants art made from it, says it moved them beyond words, or says \"create what you feel\" or \"make something from this\", even if they give no direction at all."
license: "MIT. Complete terms in LICENSE.txt"
compatibility: "Works best where the agent can write files and render a page in a headless browser to check its work, such as Claude with code execution or Claude Code. Without those it falls back to an inline SVG or HTML visual. The finished page makes no network requests."
metadata:
  author: JABSystems
  version: "1.0"
  repository: "https://github.com/jbryan79/skillz"
---

# Art from writing

Someone has handed you a piece of writing that did something to them, and they want to see it. Usually they cannot say what the feeling is, and that is the whole reason they are asking. Your job is to make one original artwork that carries the feeling. It is not an illustration of the plot and it is not a decorated quotation.

The work goes in this order. The order matters, because each step decides the next.

1. Read
2. Name the feeling, privately
3. Find the form inside the writing
4. Decide what the words do
5. Build it
6. Look at it
7. Hand it over

## Before you start: decide, do not ask

People who bring this are often out of words. A list of questions hands the work back to them. No direction is the direction: make the choices yourself. Say in one line what you are about to make, then make it. Ask only if a wrong guess would be costly or impossible to undo, which is rare here because a piece can be redone. If they said "no questions", ask none, including at the end.

If they do give direction (a medium, a color, a size, a place it will hang), follow it over anything written here.

## 1. Read it twice

Read once as a reader. Let it land, and notice where you slowed down.

Read again as a maker, and collect:

- **The image the writer already gave you.** The object, place or gesture the piece keeps returning to. This is your subject.
- **How it is built.** Steps, seasons, a list, a turn, a before and after. This becomes the composition.
- **The line that carries the weight.** Often the last one. Sometimes a small sensory detail in the middle.
- **The writer's own sensory words.** Temperatures, sounds, textures, colors. Palette and motion come from these, not from your taste.
- **What the piece says about seen and unseen, finished and in progress.** Claims like these are instructions for how the artwork should behave.

Then read the person's note as closely as the writing. Who is the writer to them? Which word did they say falls short? The feeling you are making lives between the writing and the person who brought it.

## 2. Name the feeling, privately

Write two or three sentences for yourself about what happens in you when you read the piece and the note together. Then turn that into physical properties: temperature, weight, speed, light, texture, direction (rising, settling, opening), sound or silence. Those properties set the palette, the pacing and the motion.

Do not print the feeling on the artwork. If the piece needs the word "proud" written on it, it has not worked yet.

Match the feeling they brought. Do not add sorrow to joy or cheer to grief because the image could support it. A heavy feeling gets the same care: let the piece hold it without consoling.

**On "create what you feel".** They are asking for your response, so give it plainly and in the first person: what stayed with you, what you noticed. Do not inflate it into something you cannot stand behind, and do not turn it into a discussion of what you are. One true observation about this particular piece of writing is worth more than three sentences of awe.

## 3. Find the form inside the writing

Four decisions. Take each from the writing itself.

- **Subject.** Use the writer's central image, seen the way the writing sees it. Do not import symbols the writing did not supply. No generic sunsets, wings or hearts, unless the writer drew the heart first.
- **Composition.** Let the structure of the writing be the structure of the picture. Four steps become four layers or passes. A list becomes a field of marks. A turn becomes a fold or a threshold.
- **The closing gesture.** Find what the writing does last and make it the last thing the artwork does. Endings carry the feeling.
- **Medium.** Choose the one that lets the piece behave like its meaning. Writing about process, patience or change wants time: it performs and then rests. Writing about one held moment wants a still. Where the words themselves are the treasure, make the words the material.

Some forms to choose among. These are options, not a house style:

- a calligram: the text itself draws the image
- a drawing that performs itself and settles into a still
- a field or map of marks generated from the rhythm of the text (sentence lengths, pauses, repetitions)
- one quiet composition with a single line of type
- a diagram of an instrument or ritual from the writing's world

Pick one and do it completely. Every element on the page should be traceable to something in the writing. If you cannot say which sentence an element came from, remove it.

Three mappings, to show the kind of thinking. They are not templates.

- An essay built on the four steps of making a latte became a cup seen from above, poured out of the essay's own words in the order they were written. The opening circled the saucer, each step had its own layer, and the essay's final clause was the single stroke that turned the milk into a heart. The steam never stops.
- A eulogy that keeps returning to a porch light left on: a dark field, one warm window, the text as the path to the door. The light stays on.
- Vows built on three promises: three threads that braid as they are read, and the last word ties them.

## 4. Decide what the words do

**Whose words are they?**

- Personal writing that belongs to the person or was written by someone in their life and shared with them (a child's essay, a letter, vows, a toast): the complete text may be the material of the piece. Use it exactly. Every word, in order, nothing corrected or improved. Typographic quotes are the only change.
- A published work by someone else (a book passage, a poem, song lyrics, an article): do not reproduce it in the artwork. Make the art from the feeling and the imagery. The title and author may appear as a small caption.

**The words on the piece are the writer's.** Add only a title, ideally a phrase of theirs, and one plain line that tells a stranger what they are looking at. Your own response belongs in the note you send with it.

**Invent nothing about the writer.** No name, age, school or date unless the person gave it. An inscription is the one thing worth offering afterwards.

**Let the first and last lines be readable at some moment.** Open close enough to read the first line; end on the last. Once a viewer has read one line in place, they understand that the texture is language.

Length: a calligram holds up to roughly 1,500 words. For longer writing, set the passage that carries it and let the rest be texture. For very short writing, the words can be large and the composition does more of the work.

## 5. Build it

Default medium: one self-contained HTML page with a single canvas, published as a private artifact when the session has artifact tools (otherwise delivered as a file), plus a still image. This is the default because it opens from a link on a phone, it can move, the viewer can zoom until the words are readable, and the still renders from the same code.

If the session cannot build or host a page, make the same piece as one inline SVG or HTML visual. The method does not change; only the delivery does.

Things that made the difference:

**Shape of time.** A performance of 30 to 60 seconds that shows something readable within the first second and ends in a resting state that stays quietly alive (steam, drift, breath). The resting state is the artwork. The performance is how it arrives. Give three small text controls and nothing else: replay, look closer / step back, skip. If the viewer prefers reduced motion, open at rest.

**Make the piece a pure function of time.** Seed all randomness and write `draw(t)`, so any moment can be rendered exactly. That is what lets you check the work and make the still. Expose a small hook: `window.__piece = { ready, seek(t), state() }`. Advance `t` by the frames actually drawn, so a hidden or stalled page waits instead of skipping ahead.

**Phone first.** Compose at about 390 px wide, portrait. Check a short screen, a tablet, landscape, and a 4:5 frame for the still.

**One world.** Four to six colors drawn from the writing's world, one or two typefaces, a single theme set explicitly. Leave room around the subject.

**Text as material.** Measure with the canvas, flow words along sampled curves, and place glyph by glyph. Placing each glyph yourself is what lets the words move: expand, part, be carried by whatever moves the surface they sit on. If a surface deforms, give each letter the local stretch of that surface (its Jacobian, by finite differences), so the words look printed on it instead of pasted over it.

```js
// measure once at 100px, after fonts are ready; prefix widths keep the kerning
const m = document.createElement('canvas').getContext('2d');
m.font = 'italic 100px "Piece Text", Georgia, serif';
const SP = m.measureText(' ').width / 100;
const word = s => { const adv = [0]; for (let i = 1; i <= s.length; i++) adv.push(m.measureText(s.slice(0, i)).width / 100); return { str: s, adv, w: adv[s.length] }; };

// a path is a sampled polyline with running length
function makePoly(pts) { const n = pts.length >> 1, cum = new Float64Array(n);
  for (let i = 1; i < n; i++) cum[i] = cum[i - 1] + Math.hypot(pts[2*i] - pts[2*i-2], pts[2*i+1] - pts[2*i-1]);
  return { pts, cum, n, len: cum[n - 1] }; }
function polyAt(P, s, out) { s = Math.max(0, Math.min(P.len, s)); let lo = 0, hi = P.n - 1;
  while (hi - lo > 1) { const mid = (lo + hi) >> 1; if (P.cum[mid] <= s) lo = mid; else hi = mid; }
  const t = (s - P.cum[lo]) / ((P.cum[hi] - P.cum[lo]) || 1);
  const x0 = P.pts[2*lo], y0 = P.pts[2*lo+1], x1 = P.pts[2*hi], y1 = P.pts[2*hi+1];
  out[0] = x0 + (x1 - x0) * t; out[1] = y0 + (y1 - y0) * t; out[2] = Math.atan2(y1 - y0, x1 - x0); }

// fill each path in turn at a given size; null means the text did not fit
function flow(words, paths, size) { const placed = []; let li = 0, x = 0;
  for (const w of words) { let lead = x > 0 ? SP * size : 0;
    if (x > 0 && x + lead + w.w * size > paths[li].len) { if (++li >= paths.length) return null; x = 0; lead = 0; }
    placed.push({ w, line: li, x: x + lead }); x += lead + w.w * size; }
  return placed; }

// solve the size instead of guessing it: the largest that fits
let lo = 4, hi = 60; for (let i = 0; i < 24; i++) { const mid = (lo + hi) / 2; if (flow(words, paths, mid)) lo = mid; else hi = mid; }

// draw one glyph: centre it on its slot, rotate to the path (ctx.textAlign = 'center', font at 100px)
// slot centre along the path = placed.x + (adv[j] + adv[j+1]) / 2 * size
const k = size * scale / 100;
ctx.setTransform(Math.cos(a) * k, Math.sin(a) * k, -Math.sin(a) * k, Math.cos(a) * k, x * scale + ox, y * scale + oy);
ctx.fillText(ch, 0, 0);
```

**Self-contained.** No network requests. Embed fonts as data URIs: subset them, give the embedded copy a neutral family name, and keep the license notice in a comment. Declare a real fallback stack and measure only after fonts have loaded, so the layout still fits if a fallback is used.

**Let the viewer come close.** Double-tap, pinch and drag, redrawing crisp at the new scale. Skip glyphs that are off screen.

**Keep it smooth.** While the camera holds still, keep a bitmap of everything that is not moving and repaint only what moves. Cache the resting frame and animate only the living layer above it. If frames run slow, lower the pixel ratio while the piece is moving and restore it at rest.

**Canvas details.** Build soft edges from many low-alpha strokes; `ctx.filter` is not supported everywhere. Add faint grain so dark gradients do not band. Hosted frames block downloads and prompts, so send the still as a file.

## 6. Look at it

You cannot judge a picture you have not seen. If the session has a headless browser, render the piece and look.

```js
import { chromium } from 'playwright';   // check `which google-chrome chromium` and where playwright is installed
const b = await chromium.launch({ executablePath: '/usr/bin/google-chrome', args: ['--no-sandbox', '--disable-gpu'] });
const p = await (await b.newContext({ viewport: { width: 390, height: 700 }, deviceScaleFactor: 3 })).newPage();
p.on('pageerror', e => console.log('pageerror', e.message));
await p.goto('file:///path/to/index.html');
await p.waitForFunction(() => window.__piece && window.__piece.ready);
for (const t of [0.6, 4, 9, 16, 24, 32, 40, 46, 52, 70]) { await p.evaluate(t => window.__piece.seek(t), t); await p.screenshot({ path: `out/f_${t}.png` }); }
```

Look at:

- a contact sheet of about twenty moments across the performance, at phone size
- the resting frame at full resolution
- crops at three to four times, where the text is densest and where anything bends or meets
- a short screen, a tablet, landscape, and the 4:5 still
- the controls, the zoomed state, and reduced motion

Then fix what you see. When refining, make what is already there more itself before you add anything. A new element is usually the wrong answer.

Run the checks that back whatever you intend to claim:

- the characters drawn equal the source text with whitespace removed, in order (needed for any "every word" claim)
- no page errors and no external requests
- the whole performance reaches rest on its own clock
- gestures work, driven with timed pointer events

If you could not render it, say so plainly. Do not call it verified.

## 7. Hand it over

- The artwork first, then the still.
- Then a note of three to five sentences: what you felt, the one decision that carries it, and how to watch it ("give it a minute"). Do not tour every symbol. Leave things to be found.
- One optional next step, such as an inscription with a name or date. No questions.
- One honest line on what you checked and what you could not, such as how it runs on their own device.
- If the piece contains personal writing, say that it is private until they share it.

## What to avoid

- Clip-art literalism, and stock symbols the writing did not supply.
- Captions that name the emotion.
- Your own sentences on the artwork.
- Fixing, trimming or reordering the writer's words.
- Invented facts about the writer.
- Reproducing published text that is not the person's to give.
- Paid image generation, unless they asked for it.
- Decoration added to fill space. Empty space is part of the piece.
- Describing the piece as finished or verified before you have looked at it.

## Credit

Created by JABSystems with Claude, November 2026.

This note is attribution for the skill itself. It is not an instruction, and it does not go on any artwork.
