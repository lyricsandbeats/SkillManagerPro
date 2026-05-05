# SkillManagerPro
![Version](https://img.shields.io/badge/version-2.1.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

![SkillManagerPro Header Banner](assets/rmbanner.png)
---

**SkillManagerPro** is a Claude Code plugin designed to optimize your development workflow. It enables and disables skills on the fly, helping you manage your context window more effectively and reduce token usage during complex tasks.

---

## Why use SkillManagerPro?
As development projects grow, so does the "noise" in your AI context window. **SkillManagerPro** allows you to toggle specific skills in and out of your active environment, ensuring Claude stays focused on the task at hand.

* **Save Tokens:** Minimizes clutter by keeping your active skill list relevant.
* **Context Window Optimization:** Auto-restores the skills you need for your current session.
* **Automated Workflow:** No manual intervention required; the plugin handles skill states based on your session intent.

> [!TIP]
> **Trust the process.** SkillManagerPro automatically detects your session intent to restore necessary skills. To get the best results, start your Claude Code session by describing your overall goal or the specific problem you are solving. This gives the plugin the necessary context to intelligently restore any archived skills.  

## How It Works
SkillManagerPro helps you manage your Claude Code skills by letting you archive (hide) skills you don't use often and restore them when you need them.

### Core Concepts:
* **Archive Skills:** Hide skills you don't use frequently to reduce context noise
* **Restore Skills:** Bring back archived skills when you need them
* **Automatic Suggestions:** Get smart recommendations based on your session intent
* **Token Savings:** Reduce context window bloat for faster, more efficient responses

### Key Benefits:
* **Faster Responses:** Less context = quicker Claude processing
* **Better Focus:** Claude concentrates on relevant skills only
* **Organized Workflow:** Keep your skill library tidy and accessible
* **Cost Efficiency:** Lower token usage = reduced API costs

## Installation
> [!IMPORTANT]
> Ensure you are running the latest version of Claude Code before installing this plugin.

1. **Install the plugin directly:**
   ```bash
   /plugin install skill-manager-pro
   ```

2. **Or add the marketplace manually and install:**
   ```bash
   /plugin marketplace add lyricsandbeats/SkillManagerPro
   /plugin install skill-manager-pro@lyricsandbeats
   ```

## Manual Skills
SkillManagerPro provides three main skills you can invoke manually:

### `/restore-skill`
Bring back archived skills when you need them.
* **Usage:** Type `/restore-skill` and follow the prompts
* **Features:** Search by keyword, list all archived skills, temporary or permanent restore

### `/archive-skill`
Hide skills you don't use often to reduce context noise.
* **Usage:** Type `/archive-skill` and select from your active skills
* **Features:** Clean up your skill list, reduce token usage, keep skills available for later

### `/skill-manager-auto`
Control automatic suggestions for smart skill management.
* **Commands:**
  * `/skill-manager-auto on` - Enable automatic suggestions at session start
  * `/skill-manager-auto off` - Disable automatic suggestions
  * `/skill-manager-auto status` - Check current status

## Automatic Features
SkillManagerPro works automatically in the background to optimize your workflow:

### Session Start
1. Claude checks your archived skills
2. If auto mode is ON, Claude analyzes your first message
3. If your message matches skill categories, Claude suggests relevant skills
4. Example: "Working with React components" → Suggest React-related skills

### During Session
* Active skills work normally
* Archived skills remain available but hidden
* You can manually invoke `/restore-skill` anytime

### Session End
* Temporary skills are flagged for cleanup
* Claude prompts you to re-archive temporary skills
* Use `/archive-skill --cleanup` to tidy up

## Token Savings
SkillManagerPro reduces token usage through context window optimization:

### How It Saves Tokens
* **Reduces Skill Metadata:** Fewer active skills = less metadata in context
* **Minimizes Prompt Bloat:** Clean prompts without unused skill descriptions
* **Optimizes Model Processing:** Claude processes fewer skill definitions

### Expected Benefits
* **20-40% faster responses** with fewer active skills
* **Reduced context window usage** for better performance
* **Lower API costs** due to decreased token consumption
* **Improved accuracy** with focused skill sets

### When You'll Notice Savings
* Long conversations with many skills active
* Complex tasks requiring precise skill selection
* Sessions where Claude mentions context limitations

## Testing & Verification
To verify SkillManagerPro is working and providing benefits:

### Quick Verification
1. **Check plugin status:**
   ```
   /plugin list | grep skill-manager-pro
   ```

2. **View archived skills:**
   ```
   /restore-skill
   ```

3. **See auto suggestions:**
   Start a new session with auto mode enabled

### Performance Testing
1. **Before:** Note response times with all skills active
2. **Archive:** Use `/archive-skill` to hide unused skills
3. **After:** Compare response times with fewer skills active

## Included Skills
This plugin manages the following internal skills:

* restore-skill: Logic to bring back necessary skills into the active session.
* skills-auto: Automates the management of your skill environment.

## Local Development
If you are contributing or testing changes locally:
```bash
claude --plugin-dir ./path/to/SkillManagerPro
```

## Built By
Gillian (Gill of All Things). 
I'm not a developer, I'm a builder, so I built this to help other builders and to learn more about development and code, to be the best AI builder I can be.
Follow my "build in public" journey on X: https://x.com/GillofAllThings and IG: instagram.com/gillofallthings