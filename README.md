# Fantasy Football Management — a skill for your AI assistant

This package teaches an AI assistant to run your fantasy football teams the way a good co-manager would: daily health checks, evidence-based lineup and waiver decisions with a confidence number on every call, a standing all-32 defense board, pre-lock checks tied to every kickoff, and a Tuesday recap that grades its own calls.

It contains no one's personal data, team names, or league details. Your assistant fills the templates in with yours during onboarding, and those filled files stay with you.

## What's inside

- `SKILL.md` — the operating method: authority modes, verified league settings, the decision rules, reporting, and grading.
- `skill.yaml` — the skill descriptor, for assistants that use one.
- `references/decision-frameworks.md` — how lineup, waiver, and defense calls get made and graded.
- `references/weekly-cadence.md` — the week's schedule of checks, from the Tuesday recap to the Monday night pre-lock check.
- `references/onboarding.md` — the intake your assistant runs with you first: leagues, verified settings, authority modes, preferences, schedule.
- `templates/` — blank working files your assistant fills in for you: one settings file per league, the defense board, and the daily check format.

## How to use it

1. Give the whole folder to your AI assistant and tell it: "Install this as a skill, then onboard me using references/onboarding.md."
   - On Muse, the folder goes in your custom skills directory (`~/workspace/custom-skills/fantasy_football_management/`).
   - On any other assistant that accepts instructions or files, upload or paste `SKILL.md` and the three reference files, and have it keep the templates as its working files.
2. Answer the onboarding questions (about fifteen minutes). Your assistant verifies your league settings live on the platform — waiver rules especially, because they decide the whole waiver strategy.
3. Pick, per league, whether the assistant runs it fully or only recommends. You can set different leagues differently.
4. Your first week runs in shadow mode: recommendations only, everywhere, so you can judge the calls before anything touches your roster.
5. From week two, the cadence runs itself. You get a short brief each morning, a waiver preview on Tuesday evening, and pre-lock checks before Thursday, Sunday, and Monday games.

## What makes it different

- **Every call carries a confidence number** (0 to 100), so you can see at a glance what is a lock and what is a coin flip.
- **No decision rides on one input.** Lineups weigh projection, past production, and expected performance from schedule, injuries, and role changes. Waiver adds weigh percent owned, trends, season totals, positional rank, and consistency, not just this week's projection.
- **Same-day rule.** A time-sensitive free agent is acted on or brought to you the day it is spotted, never parked behind a later reminder.
- **It grades itself.** Tuesday's recap scores the week's calls on process and outcome separately, and recurring mistakes rewrite the frameworks.
- **Your settings are verified, never assumed.** The assistant re-checks waiver mechanics and limits live before quoting them, because acting on a misremembered league rule is the fastest way to lose a season and your trust.

Good luck this season.
