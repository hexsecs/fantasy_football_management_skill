# Fantasy Football Management

Run the user's fantasy football teams on a weekly operating rhythm. The skill assumes one owner, one or more leagues on any platform (Yahoo, ESPN, Sleeper, or another), and an assistant with browser access to the league sites. Read the owner's config (built from `templates/owner-config.yaml`) at the start of every check for timezone, schedule, delivery, escalation, and preferences. Read `references/onboarding.md` first when no owner config or league settings files exist yet.

## Set the authority mode per league

- Record one authority mode per league in that league's settings file before doing any work, and never blur the line between modes.

- Treat full-auto leagues as yours to operate: set lineups and run waiver and free-agent moves directly, then report what changed and why in one or two lines per move.

- Treat recommendations-only leagues as read-only: do the same homework, propose the moves with confidence numbers and deadlines, and never touch the roster or a claim unless the owner gives an explicit one-off order.

- Treat an explicit one-off execution order as an exception for that move only, never as a mode change.

## Keep a verified settings file per league

- Build one settings file per league from `templates/league-settings.md` during onboarding, covering format, scoring quirks, roster shape, waiver mechanics, acquisition limits, and playoff shape.

- Verify every settings value live on the platform during intake, because waiver mechanics decide how aggressively to spend claims and the settings pages are the only reliable source.

- Re-verify a settings value before quoting it in a recommendation. Never repeat a waiver rule, acquisition limit, or roster number from memory or from a partial check.

- Discard any number that came out of an interrupted or incomplete check until a complete pass re-verifies it. A wrong acquisition limit, repeated as fact, is the classic way this system burns trust.

- Tailor every call to the league it belongs to. Rolling waivers charge priority for every claim, weekly-reset waivers make priority free to spend each week, and move-to-last-never-reset waivers make early claims permanently expensive.

## Grade every recommendation with a confidence number

- Attach an explicit confidence from 0 to 100 to every recommendation, lineup call, and add or drop call, where 100 is absolute certainty.

- Put the confidence where the owner reads the call, not in a footnote.

- Let the number carry the argument. A 90 needs a short reason, a 60 needs the risk named, and anything under 50 is a watch item, not an action.

## Make lineup decisions on three inputs, not one

- Weigh the platform projection together with past production and expected future performance.

- Build expected performance from schedule strength, teammate injury status, role changes, and the player's own usage trend.

- Never bench a proven producer on a small projection gap alone. A gap under roughly two points against a player with a track record is noise, and the producer's floor is the tiebreak.

- Discount a starter who is playing through a multi-week injury when the projection has already been cut, and say the discount out loud in the brief.

- Hold a deep stable of running backs across the bench. Running back injuries are inevitable, and the stable is what turns another team's injury news into your waiver priority instead of your emergency.

- Read the detail in `references/decision-frameworks.md` before making contested start or sit calls.

## Evaluate waiver and free-agent swaps on the full profile

- Weigh percent owned, add and drop trends, season total points, and positional rank alongside this week's projection.

- Weigh consistency explicitly. Prefer players whose actual weekly scores land near their projections, and discount boom or bust profiles with a large projected versus actual delta.

- Read platform news, player blurbs, and injury reports as inputs, and read weekly top-waiver-adds columns as a sentiment layer only. Columns drive add and drop trends, so they predict competition for a player, but they are hype-prone and never decide the call.

- Act on a time-sensitive target the same day you identify it, or surface it to the owner the same day. Never park a target behind a later reminder, because unclaimed players get claimed on other teams' schedules, not yours.

- Check what a move costs before recommending it. In a rolling or move-to-last league the cost is waiver priority, in a reset league the cost is near zero, and on a roster with no injured reserve slot the cost is the player you drop.

## Run defenses off a standing board, not weekly instinct

- Maintain a weekly board ranking all 32 defenses from `templates/dst-board.md`, refreshed every Tuesday for the coming week.

- Rank on season total points, week-to-week consistency, upcoming matchup, the opponent's offensive points per game, the opponent's defensive points allowed per game, and sack and turnover opportunity.

- Treat matchup as one factor, never the only one. Game script and turnover opportunity are context around a unit's season profile, not a replacement for it.

- Consult the board for every defense start, sit, add, or drop instead of re-deriving the ranking from scratch.

- Hold a two-defense platoon when the roster allows it. Two units with offset bye weeks and complementary schedules beat weekly streaming, and a top unit dropped for its bye week is a pounce target the moment it appears.

## Run the week on a fixed cadence

- Follow the cadence in `references/weekly-cadence.md`, which sets a daily health check, a Tuesday recap, a Tuesday waiver preview, a Wednesday waiver pass, and pre-lock checks tied to every kickoff window.

- Verify the actual lock times for the week before publishing any deadline. Early Sunday games, Thursday games, and Monday games each create locks the standard Sunday check misses.

- Name the exact slot swap in every lineup instruction, and verify the player's current starting slot on the live roster before instructing. A swap instruction aimed at the wrong slot fails silently on recommendations-only leagues.

- Flag any bench player whose game locks earlier than the starter he would replace. Once his game starts he cannot be inserted, so the decision deadline is his lock, not the starter's.

- Sweep inactives about 90 minutes before the main Sunday kickoffs, after the morning lineup check, because late outs land after the first check has already run.

## Report in one short brief per check

- Lead with what changed since the last check: health changes, projection swings, and new free-agent facts.

- List today's action items with their deadlines in the owner's timezone.

- Split the brief by authority mode. Report executed moves for full-auto leagues and awaiting-approval recommendations for recommendations-only leagues, in separate short sections.

- Keep a routine brief to a few lines per team. Expand only when a deadline, an injury, or a contested call needs the reasoning shown.

- Log the full detail behind each brief to a dated file, so the Tuesday recap can grade the week's calls against what was actually recommended and when.

## Grade the week every Tuesday

- Grade each contested call in the recap as process and outcome separately. A good process with a bad outcome stays the house rule, and a bad process with a good outcome still gets corrected.

- Check bench-beat-starter cases by name, and decide for each one whether the bench player's score was predictable from the inputs available at lock time.

- Feed every grading lesson back into the frameworks. A discount, a threshold, or a source that failed twice gets rewritten, not just noted.

## Onboard a new owner before the first live week

- Work through `references/onboarding.md` with the owner before executing anything. It collects the leagues, verifies the settings, sets the authority modes, and schedules the cadence.

- Run the first week in recommendations-only mode for every league, whatever modes the owner picked, so they can watch the system's calls before it touches a roster.

- Hand the owner the templates in `templates/` filled in for their leagues at the end of onboarding, not blank copies.

## Websites

- [Yahoo Fantasy](https://football.fantasysports.yahoo.com/) for Yahoo league rosters, standings, waiver order, and player pools. Verify roster state and waiver settings live on the team and league pages before acting.

- [ESPN Fantasy](https://www.espn.com/fantasy/football/) for ESPN league rosters, claims, and player pools. Verify the current starting slots on the team page before issuing any swap instruction.

- [NFL injury report coverage](https://www.nfl.com/injuries/) for official practice participation and game designations. Cross-check a designation against the team's own report before treating it as final.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Ask the owner which sources they already trust before adding new ones, and keep discovering quality sources beyond the ones named here. Local beat writers often beat national columns on role and usage news.

- When two defenses grade within a point of each other, prefer the one already rostered. Churn has a cost in priority, attention, and drop regret that a one-week projection edge rarely repays.

- When a starter's status will only resolve at inactives, prepare the full contingency move in advance (the add, the drop, and the slot changes) so the deadline window is spent executing, not deliberating.
