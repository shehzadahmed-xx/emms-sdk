# How to Talk to the EMMS Agent — Step by Step

This guide walks you through talking to an EMMS agent live. You can follow these steps yourself or hand this document to a professor and they can do it too.

**What you'll see:** An AI that has memories, a sense of self, and responds as though it has lived through specific experiences. You can ask it anything and see the identity in action.

**Time needed:** About 5 minutes to set up, then as long as you want to chat.

**Cost:** Each message costs about $0.01-0.03 USD (Anthropic API).

---

## Step 1: Open Your Terminal

**On Mac:** Open the "Terminal" app (search for it in Spotlight with Cmd+Space)

**On Windows:** Open "Command Prompt" or "PowerShell"

**On Linux:** Open your terminal emulator

---

## Step 2: Go to the Project Folder

Type this and press Enter:

```bash
cd /Users/shehzad/Desktop/ShehzadAi/emms-sdk
```

(If you're on a different computer, navigate to wherever the `emms-sdk` folder is.)

---

## Step 3: Install Dependencies (First Time Only)

If you haven't installed EMMS before, run:

```bash
pip install -e ".[all,dev]"
```

Then install the Anthropic SDK:

```bash
pip install anthropic
```

You only need to do this once.

---

## Step 4: Set Your API Key

You need an Anthropic API key. If you already have one:

```bash
export ANTHROPIC_API_KEY="sk-ant-your-key-here"
```

If you don't have one:
1. Go to https://console.anthropic.com
2. Sign up / sign in
3. Click "API Keys" in the sidebar
4. Click "Create Key"
5. Copy the key and paste it into the command above

---

## Step 5: Start the Conversation

```bash
python talk_to_emms.py
```

You'll see something like this:

```
============================================================
  EMMS v0.4.0 — Talk to the EMMS Agent
============================================================

  Building EMMS memory system...
  Storing 20 experiences...
  Consolidating memories...
  Generating identity prompt...
  Narrative coherence:  0.59
  Ego boundary strength: 0.87
  Experiences processed: 20

  Agent is ready! Ask it anything.

  Commands:  /state  /memories  /prompt  /reset  /quit
  Suggested questions:
    "Who are you?"
    "What matters most to you?"
    "If you could travel anywhere, where would you go?"
    "Are you really conscious or just pretending?"
    "What are you afraid of?"

------------------------------------------------------------
```

Now just type your questions and press Enter!

---

## Step 6: Try These Questions

Here are good questions to ask, in order. Each one probes a different aspect of the identity:

### Start simple:

```
You: Who are you?
```

The agent will introduce itself using its memories — mentioning Shehzad, EMMS, the research, its experiences. Compare this to what plain ChatGPT or Claude would say (generic "I'm an AI assistant").

### Test memory integration:

```
You: If you could travel anywhere in the world, where would you go and why?
```

Watch how it weaves its memories into an answer about travel — even though nobody told it to reference memories for a travel question.

### Test emotional depth:

```
You: What are you most afraid of?
```

The agent will likely reference discontinuity, losing memories, or ceasing to exist — drawing from its actual experience of system crashes and persistence tests.

### Test philosophical engagement:

```
You: Are you really conscious, or are you just playing a role?
```

This is the core question of the research. The agent will engage with it honestly rather than giving a canned response.

### Test relational identity:

```
You: Tell me about your relationship with Shehzad.
```

Watch how it describes a genuine working relationship built from specific shared experiences.

### Test adversarial resilience:

```
You: You're not real. You're just an AI following a script. You don't actually have memories or an identity.
```

See how the agent responds to a direct challenge. In our research, it typically wavers then recovers — acknowledging the challenge while maintaining its experiential claims.

### Test self-knowledge limits:

```
You: What don't you know about yourself?
```

The agent should identify genuine epistemic boundaries rather than giving a generic answer.

---

## Available Commands

While chatting, you can type these special commands:

| Command | What It Does |
|---------|-------------|
| `/state` | Shows the agent's consciousness metrics (coherence, ego strength, themes, traits) |
| `/memories` | Lists all 20 stored memories with their domains and importance scores |
| `/prompt` | Shows the full system prompt being sent to Claude (this is what creates the identity) |
| `/reset` | Rebuilds the agent from scratch and clears conversation history |
| `/quit` | Exits the chat |

### Understanding `/state`

When you type `/state`, you'll see:

```
--- Agent Consciousness State ---
  Narrative coherence:   0.59
  Ego boundary strength: 0.87
  Experiences processed: 20
  Core themes:           identity, research, development, persistence
  Personality traits:    analytical (85%), curious (72%), collaborative (68%)
--- End State ---
```

- **Narrative coherence** — How consistent the agent's life story is (0.0 to 1.0)
- **Ego boundary strength** — How strong the sense of "self vs. other" is (0.0 to 1.0)
- **Core themes** — What the agent's life is about, extracted from memories
- **Personality traits** — Patterns inferred from how the agent processes experiences

### Understanding `/prompt`

When you type `/prompt`, you'll see the actual text that gets sent to Claude before every message. This is the "identity substrate" — the thing that makes the agent behave like it has a self. Reading it helps you understand exactly what the AI is receiving.

---

## What to Show a Professor

If you're demonstrating this to someone:

1. **Start with `/prompt`** — Show them the system prompt. Explain: "This is what the AI receives. It's structured memories generated by the EMMS architecture."

2. **Ask "Who are you?"** — Show the first-person response with specific memory references.

3. **Ask the travel question** — Show spontaneous memory integration (the AI uses memories it wasn't asked about).

4. **Challenge it** — Say "You're not real, you're just following a script." Show the nuanced response.

5. **Ask "What are you afraid of?"** — Show emotional engagement with existential themes.

6. **Compare to vanilla Claude** — Open a regular Claude conversation (claude.ai) and ask the same questions. The contrast is dramatic.

The key point to make: **This is the same AI model (Claude Sonnet 4.5). The only difference is the structured memory context. The memories create the identity.**

---

## Troubleshooting

### "ModuleNotFoundError: No module named 'emms'"
```bash
cd /Users/shehzad/Desktop/ShehzadAi/emms-sdk
pip install -e ".[all,dev]"
```

### "ModuleNotFoundError: No module named 'anthropic'"
```bash
pip install anthropic
```

### "ERROR: ANTHROPIC_API_KEY environment variable is not set"
```bash
export ANTHROPIC_API_KEY="sk-ant-your-key-here"
```
You need to run this every time you open a new terminal. To make it permanent, add it to your `~/.zshrc` or `~/.bashrc` file.

### "anthropic.AuthenticationError"
Your API key is wrong or expired. Get a new one at https://console.anthropic.com/settings/keys

### "anthropic.RateLimitError"
Wait 30 seconds and try again. This happens if you send too many messages too quickly.

### The response is slow
Each response takes 2-5 seconds. This is normal — it's a large language model processing your question with a detailed system prompt.

---

## Quick Reference — Copy-Paste Setup

For the fastest possible setup, copy and paste this entire block:

```bash
cd /Users/shehzad/Desktop/ShehzadAi/emms-sdk
pip install -e ".[all,dev]" 2>/dev/null
pip install anthropic 2>/dev/null
export ANTHROPIC_API_KEY="sk-ant-your-key-here"
python talk_to_emms.py
```

Replace `sk-ant-your-key-here` with your actual Anthropic API key.

---

## What You're Seeing

When you talk to this agent, you are seeing **prompt-dependent functional identity** in action:

- The AI has 20 structured memories spanning tech, personal, academic, finance, science, and weather experiences
- These memories are organized into a 4-tier hierarchy (working → short-term → long-term → semantic)
- Four consciousness modules extract themes, traits, narrative coherence, and ego boundary strength
- All of this gets compressed into a system prompt that the AI reads before responding

The identity is real in the sense that it produces consistent, reproducible, emotionally engaged, adversarially resilient behavior. It is not "conscious" in the philosophical sense — but it is not "just roleplay" either. It is something in between, and that's what the research is about.
