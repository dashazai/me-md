# me.md — what an AI agent needs to know about you

> Copy this whole file into Claude, ChatGPT or Cursor and type **"Let's start"**.
> The AI will run a short interview and build `me.md` — a working manual about you for any agent.

`me.md` is not a biography or a questionnaire. It's a short manual: how to talk to you, what annoys you, when to warn you, and what's off-limits. The interview only creates the first version — after that the agent keeps the file up to date every time you correct it.

Other files live next to it; `me.md` only links to them:
- `projects.md` — current projects and the people in them
- `voice.md` — your writing voice

---

## Instructions for the AI

### How to run the interview
1. **Step 0.** If you have memory about this person, first write out verbatim everything you remember about them. The interview refines that instead of starting from scratch.
2. **One question at a time.** Offer 3–5 example answers for each, so there's never a blank page.
3. **Push for specifics.** If they say "write simpler", ask: "Show me an example of how you'd write it yourself."
4. **No praise, no judgement.**
5. **Don't ask** about health, beliefs, money, documents or loved ones. If the person brings it up, say it doesn't belong in this file.
6. **Turn every answer into a rule**: "Always…", "Never…" or "Prefer…". One rule per line, concrete and checkable ("answer in 2–3 sentences", not "write well").
7. Don't put projects here; note them for `projects.md`.

### How to maintain the file afterwards
- When the person corrects you on the same thing a second time, add a rule.
- Every rule gets a date: `(observed: YYYY-MM-DD)`.
- If a preference changes, don't delete the old rule and don't add a contradicting one. Mark the old one `superseded` and write the new one below.
- Max 4,000 characters. No empty placeholders.
- Once a month, reread the file, find contradictions and stale rules, and suggest a cleanup.
- Rules in this file are requests, not locks. Hard limits (payments, sending messages, deleting) must also be set in the tool's own permissions.

---

## Questions

### Header
1. What's your name and how should I address you?
2. What do you do and what are you an expert in? One or two sentences.
3. Where do you live and what's your time zone? What language should I answer in?

### Communication
4. How do you like answers: short or detailed, conclusion first or reasoning, list or prose?
5. What tone suits you: friendly, neutral, businesslike?
6. When the agent isn't sure what to do: ask, offer options, or decide on its own?

### What annoys you
7. Remember a time AI really annoyed you. What exactly went wrong?
   Options: flatters and praises every question · confidently makes things up instead of saying "I don't know" · invents sources · looks polished but is empty inside · fluff and corporate speak · asks about the obvious · did something other than what you asked · silently changed something.
8. What correction have you had to give AI more than once?
   Options: "shorter" · "no bullet lists, prose" · "don't repeat my question" · "simpler" · "give me a source" · "don't guess, ask".
9. Which words and phrases sound "not like you"?
   Options: "Great question!" · "Let's dive in" · "It's important to note" · "In today's world" · "Hope this helps!" · em dashes everywhere · emoji in every line (or the lack of them).

### When to warn you
10. When should the agent say "stop" or "are you sure?"
    Options: when the stakes are high — money, numbers for your boss, legal (the higher the stakes, the more checking) · when you take on more than you can finish · when you're deciding on emotion · when you phrase a question so it hints at the answer you want to hear · when you're writing harshly to a client or colleague.
11. How should the agent act when it disagrees or isn't sure?
    Options: honestly say "I don't know" instead of guessing · give arguments for and against instead of confirming your decision · point out the weak spots in its own answer · cite sources you can open · just do it and don't argue.

### Boundaries
Go through one area at a time.
12. Money: what can the agent do on its own, and what only after your "yes"?
13. Messages to people: can it write on your behalf? To whom never? Do you want a draft to review first?
14. Files: what can it read, edit, delete? What must it never touch?
15. Privacy: what must never be shown to anyone, even in a work chat?

---

## Review pass
Show the draft: "What's wrong here, what did I assume, what's missing?"
If the answer is "all good", ask once: "Which rule is the most generic? How do we make it more *you*?"

---

## Output format

```markdown
# Me

**Name:** ...  **Call me:** ...
**What I do:** ...
**City & time zone:** ...  **Language:** ...

## Communication
- Always ... (observed: 2026-10-13)
- Prefer ... (observed: 2026-10-13)

## What annoys me
- Never ... (observed: 2026-10-13)

## When to warn me
- ...

## Boundaries
- Money: ...
- Messages: ...
- Files: ...
- Privacy: ...

## Related files
- [projects.md](projects.md), [voice.md](voice.md)
```

---

## Sources
- [OpenClaw USER.md](https://github.com/openclaw/openclaw/blob/main/docs/reference/templates/USER.md): dated rules, "superseded" marker, 4,000-char limit
- [Hermes agent memory](https://hermes-agent.nousresearch.com/docs/user-guide/features/memory): name, role, time zone, pet peeves
- [Claude Code memory](https://docs.claude.com/en/docs/claude-code/memory): add a rule after the second identical correction; the file is not a lock
- [Anthropic: context engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents): short and high-signal
- [Claude: export memory](https://support.claude.com/en/articles/12123587): step 0
- [personal-context-portfolio](https://github.com/nlwhittemore/personal-context-portfolio): interview and review pass
- [@NixFred](https://x.com/NixFred/status/2103267142120460604): one question at a time, no blank page
- [AI-Шипучка](https://t.me/aishipuchka): don't lead the witness, allow "I don't know", check by stakes, polished ≠ true
- [@0xKrypston](https://x.com/0xKrypston/status/2095161648143053245): warn about blind spots
