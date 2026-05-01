# SkillManagerPro

**SkillManagerPro** is a Claude Code plugin designed to optimize your development workflow. It enables and disables skills on the fly, helping you manage your context window more effectively and reduce token usage during complex tasks.

---

## Why use SkillManagerPro?
As development projects grow, so does the "noise" in your AI context window. **SkillManagerPro** allows you to toggle specific skills in and out of your active environment, ensuring Claude stays focused on the task at hand.

* **Save Tokens:** Only load the skills you need for your current task.
* **Reduce Context Window:** Strip away unnecessary instructions and files.
* **Modular Design:** Keep your `skills/` directory organized and clean.

## Installation

Add this repository to your Claude Code marketplace to install:

1. **Add the marketplace:**
   ```bash
   /plugin marketplace add lyricsandbeats/SkillManagerPro-V1

2. **Install the plugin:**
   ```bash
   /plugin install skillmanagerpro-v1@lyricsandbeats

## Usage
* skill-enable <name>: Activate a specific skill.
* skill-disable <name>: Remove a skill from your active context.

## Local Development
If you are contributing or testing changes locally:
```bash
claude --plugin-dir ./path/to/SkillManagerPro-V1

Built by Gillian (Gill of All Things).
Follow my "build in public" journey on X: https://x.com/GillofAllThings and IG: instagram.com/gillofallthings






