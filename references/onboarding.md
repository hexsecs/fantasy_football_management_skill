# Onboarding a new owner

Work through this once, before the first live week. The whole intake takes about fifteen minutes of questions plus one live verification pass per league. Do not execute any roster move until onboarding is complete.

## Step 1: Collect the leagues

Start the owner config from `templates/owner-config.yaml` with the owner's timezone and one `leagues` entry per league. Then ask for each league separately, and record the answers in a settings file built from `templates/league-settings.md`:

- Platform (Yahoo, ESPN, Sleeper, or other) and how the assistant will access it (the owner's signed-in browser session is the usual route).
- League name or ID and the owner's team, exactly as they appear on the platform.
- Number of teams, head-to-head or points format, and the scoring system (PPR, half PPR, standard, or custom).
- Roster shape: starters by position, bench size, injured reserve slots, and any position maximums.
- Waiver system: rolling priority, weekly reset, move-to-last, or FAAB. The waiver period length and the processing day and time.
- Acquisition limits: per week, per season, and on trades. Ask, then verify live in Step 2 regardless of the answer.
- Playoff weeks and format.
- Any league the owner wants ignored entirely (an accidental signup, a league they play casually). Record ignored leagues explicitly so the system never manages them by mistake.

## Step 2: Verify the settings live

- Open each league on its platform and read the settings from the league's own settings page, not from the owner's memory or a summary screen.
- Confirm the waiver mechanics, the processing time, and the acquisition limits character by character. These three values decide the waiver strategy, and they are the values most often carried wrong.
- Read the owner's current roster, record, waiver priority, and standing while you are there. That snapshot is the baseline the first brief compares against.
- Mark every value in the settings file as verified, with the date. An unverified value stays visibly marked until a complete pass confirms it.

## Step 3: Set the authority modes

- Ask, per league, whether the assistant operates it fully (lineups and claims executed, then reported) or recommends only (nothing touched without approval).
- Default to recommendations-only for any league the owner hesitates on. A mode can be loosened later in one sentence, and trust is easier to build than to rebuild.
- Record the modes at the top of each settings file, where every later check reads them first.

## Step 4: Agree on preferences and house rules

- Walk the owner through the frameworks in `references/decision-frameworks.md` and ask which they want changed. The common tuning points:
  - Risk posture on questionable starters (start the upside or take the healthy floor).
  - Bench philosophy, including how deep a running back stable they want held.
  - Defense strategy (hold a platoon, stream weekly, or hold one top unit through its bye).
  - Whether trade exploration is in scope at all. It is out of scope by default.
  - Sources they already trust for news and rankings.
- Write owner-wide answers into the owner config (`templates/owner-config.yaml`) and league-specific ones into that league's settings file. Preferences the owner stated once should never need stating twice.

## Step 5: Set the schedule

- Offer the cadence from `references/weekly-cadence.md` with its default times, in the owner's timezone, and adjust the clock times to their mornings and evenings.
- Confirm how briefs should arrive (chat, email, or another channel) and how recommendations-only approvals come back (a reply, a tap, or the owner executing silently).
- Record the agreed times, delivery, and escalation in the owner config's `schedule`, `delivery`, and `escalation` sections.
- Confirm the escalation rule for deadline windows: if a Thursday or Sunday contingency needs the owner's word and they do not answer before the lock, the default is no move on recommendations-only leagues, and the prepared best-judgment move on full-auto leagues.

## Step 6: Shadow week

- Run the first week with every league in recommendations-only mode, whatever the owner picked. The owner sees the briefs, the confidence numbers, and the grading before the system touches a roster.
- At the end of the shadow week, walk the Tuesday recap together, confirm the modes for week two, and only then enable full-auto execution where chosen.

## Step 7: Hand over the working files

- Give the owner their filled-in owner config and settings files, the first defense board built from `templates/dst-board.md`, and one sample daily brief built from `templates/daily-check.md`, so they can see exactly what the system keeps and produces.
- Tell the owner the three things that will make the system better over the season: correcting a call in the moment (the correction gets folded into the frameworks), naming sources they trust, and answering the graded recap when a process call surprises them.
