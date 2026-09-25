# pr0mtsy

A universal prompt that turns any topic into a MAXIMAL, complete
answer. Works with any LLM chat interface. Starts with a numbered
question round, supports SK!P commands to skip questions, and
delivers deep, structured output on any topic.

[Prompt](pr0mpt.md) | [License](LICENSE) | [Contributing](CONTRIBUTING.md) | [Changelog](CHANGELOG.md) | [Security](SECURITY.md)

---

## Supported LLMs

Works with any chat interface that lets you send a text message:

- ChatGPT
- Claude
- Gemini
- Grok
- Mistral
- DeepSeek
- Perplexity
- Local models (Ollama, LM Studio, etc.)
- Any other chat-based LLM

The only requirement: you can paste text into the chat window.

---

## How to Use

**Important:** This prompt is too long for most "Custom
Instructions" fields. Instead, paste it directly into the chat
window as your first message.

### Step by Step

1. Open your preferred LLM chat.
2. Start a new chat.
3. Open [pr0mpt.md](pr0mpt.md) in this repository.
4. Click the copy icon in the top-right corner of the code block.
5. Paste the entire prompt into the chat window.
6. Send it.
7. Now write any topic in the next message.

That's it. The prompt will now run for the rest of the conversation.

### Do NOT paste it into

- Custom Instructions fields - too long
- System prompt fields - not needed
- Memory or similar fields - wrong place

It belongs in the **chat window**, as your first message.

---

## What It Does

The prompt turns any topic into a MAXIMAL, complete answer in three
phases:

1. **Question round** - The model asks 6-12 numbered clarifying
   questions before producing any content.
2. **Skip commands** - You can skip one, several, or all questions.
3. **MAXIMAL delivery** - Once the question round is done, the model
   delivers a complete, structured answer with no length limit.

---

## Skip Commands

| Command | Effect |
|---------|--------|
| `SK!P` | Skips the next question |
| `SK!P 2` | Skips the next 2 questions |
| `SK!P 3` | Skips the next 3 questions |
| `SK!P all` | Skips all remaining questions |
| `SK!P [No]` | Skips question number X specifically |

Skipped questions get a sensible assumption, which the model marks
with `[ASSUMPTION]` in the evaluation step.

---

## Scope Levels

| Level | Content | Extras | Length |
|-------|---------|--------|--------|
| Little | Minimal answer | No | Short |
| Medium | Solid answer | Few | Medium |
| Lots | Detailed | Yes | Long |
| MAXIMAL | Everything, full | All | Unlimited |

---

## Features

- Works with any LLM chat interface
- Numbered question round before every answer
- Skip commands: SK!P, SK!P 2, SK!P 3, SK!P all, SK!P [No]
- Explicit [ASSUMPTION] tracking for every skipped question
- MAXIMAL mode: no length limit, full structure
- Language chosen by the user at the start of the conversation
- No emojis, plain Markdown only

---

## FAQ

**Which LLMs does this work with?**
Any chat-based LLM where you can paste text: ChatGPT, Claude, Gemini,
Grok, Mistral, DeepSeek, Perplexity, local models, and more.

**Why can't I put this in Custom Instructions?**
The prompt exceeds the character limit of most Custom Instructions
fields. Paste it into the chat window instead.

**Do I have to paste it every time?**
Yes. Every new chat starts fresh, so paste the prompt at the start
of each new conversation.

**Does it work on mobile?**
Yes. Copy the prompt from [pr0mpt.md](pr0mpt.md), open your LLM app,
paste it into a new chat.

**What if I do not want any questions?**
Write `SK!P all -> MAXIMAL` after your topic.

**Why no emojis?**
Because the output is meant to be clean, copy-pasteable, and
readable in any context.

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to contribute.

---

## License

This project is source-available, not open source.

You may use it for personal, educational, and internal business
purposes. You may modify and adapt it for your own use.

You may NOT redistribute, publish, share, sublicense, or resell
this prompt in original or modified form.

See [LICENSE](LICENSE) for the full text.

---

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for version history.

---

## Security

See [SECURITY.md](SECURITY.md) for how to report issues.
