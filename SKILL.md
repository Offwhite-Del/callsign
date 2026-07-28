---
name: callsign
description: Generate human-aesthetic names for anything — repos, products, skills, tools, features, projects, pets, Wi-Fi networks. Use when the user asks to name something, brainstorm names, rename, pick a codename, or evaluate name candidates. Triggers include "起个名", "叫什么名字好", "帮我想个名字", "name this", "naming", "rename", "codename".
metadata:
  version: "1.0.0"
---

# callsign

Naming is taste, not thesaurus. A good name survives being said aloud in a meeting, typed into a terminal, and searched on Google.

## What makes a name good

1. **Sayable** — passes the phone test: say it once, the listener can spell it.
2. **Spellable** — no ambiguous letters (ph/f, c/k), no forced double letters, no keyboard gymnastics.
3. **Short** — 1-3 syllables for products/tools; compound lowercase-hyphen for repos is fine.
4. **Evocative over descriptive** — `stripe`, `linear`, `raycast` suggest a feeling; `fast-payment-api` describes a spec. Metaphors age better than features.
5. **Room to grow** — don't name v1 after its only feature (`pdf-merger` dies when it also splits).
6. **Searchable** — common dictionary words need a twist (`vercel` not `vercel-hosting`); coined words need to still be pronounceable.

## Process

1. **Extract the essence**: ask (or infer) what the thing does, who it's for, and the *feeling* it should give (fast? tidy? calm? powerful? playful?). One sentence max.
2. **Generate wide, across registers** — at least three of these:
   - Metaphor: domain-adjacent imagery (`loom`, `sentry`, `tide`)
   - Coined: short invented words that sound like the feeling (`v0`, `supabase`)
   - Compound: two crisp words fused (`vercel` = versatile+excel, `netlify`)
   - Plain-word twist: real word, new job (`notion`, `obsidian`, `clerk`)
   - Heritage: mythology/astronomy/latin — sparingly, only if it fits the brand
3. **Filter ruthlessly** against the six criteria above. Kill anything you'd need to spell twice.
4. **Check collisions** before presenting: `gh search repos <name>` for repos, and note if the .com/.dev/.sh is obviously taken by a major product. Don't promise availability — say "checked, no major collision".
5. **Present 6-10 candidates**, grouped by register, one line each: the name, why it works, one honest watch-out. Mark your top pick and say why. Let the user decide — taste is theirs.

## Pitfalls

- No `-ify`/`-ly`/`AI-` prefix salad unless it genuinely fits.
- No inside jokes that embarrass you in six months; no names you'd hesitate to say to a client.
- Match the ecosystem: CLI tools tolerate hyphens and lowercase; consumer products need a capitalizable word; skills/plugins want `kebab-case` that reads as a verb or noun, not a sentence.
- Chinese-English mixed audiences: check the name doesn't romanize into something awkward in pinyin, and that a Chinese gloss exists if the user needs one.

## Output format

```
**意境组**
- name — 为什么成立（一句话）；注意点

**造词组**
- ...

推荐: X — 理由
```
