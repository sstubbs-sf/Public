I've been given a Cortex Code skill as a zip file: solventum-html-slides.zip
Please install it into CoCo Desktop for me.

The zip contains a single top-level folder named `solventum-html-slides`.
Skills live in `~/.snowflake/cortex/skills/`.

Please:

1. Check whether `~/.snowflake/cortex/skills/solventum-html-slides` already exists.
   - If it does, move it aside to `solventum-html-slides.backup-<today's date>`
     first. Do NOT merge the new files into the old folder — a merge leaves stale
     icons and stale scripts behind, and the skill's own docs would then disagree
     with what's on disk.
   - Tell me if you found an existing one and what you did with it.

2. Extract the zip so the result is exactly:
   `~/.snowflake/cortex/skills/solventum-html-slides/SKILL.md`
   (not nested twice, e.g. `.../solventum-html-slides/solventum-html-slides/`).

3. Verify the install actually works — don't just confirm the files copied:
   - `python3 ~/.snowflake/cortex/skills/solventum-html-slides/scripts/test_gates.py`
     must report **35/35 controls passed**.
   - `ls ~/.snowflake/cortex/skills/solventum-html-slides/assets/icons | wc -l`
     must report **326**.
   - `python3 .../scripts/check_deck.py .../examples/example-deck.html`
     must report **PASS**.
   If any of those three disagree, stop and tell me — the extract is incomplete.

4. Tell me I need to restart CoCo Desktop (or start a new session) for a newly
   installed skill to be picked up.

Then confirm what the skill does and how I invoke it.
