# Decision frameworks

The detailed evaluation logic behind the calls in SKILL.md. Every framework ends in a confidence number from 0 to 100.

## Lineup decisions (start or sit)

Weigh three inputs together:

1. **Projection.** The platform's projection for this week, in this league's scoring. Projections are the starting point, not the answer.
2. **Past production.** The player's actual weekly scores this season, with the trend weighted more than the average. A player whose last three weeks beat his season average is a different asset than one fading the other way.
3. **Expected performance.** A forward estimate built from schedule strength, teammate injuries, role changes, and usage. Examples of adjustments that move this number: a receiver whose team's top option is out (target share up), a running back whose backfield mate is limited (snap share up, or committee risk up), a quarterback facing a defense that funnels passing volume.

House rules:

- Never bench a proven producer on a small projection gap alone. Under roughly two points, start the track record.
- A questionable tag is not a benching. Read the practice week: full participation by Friday usually means a full role, a week of did-not-practice usually means a limited role or an inactive, and limited all week is the genuinely uncertain middle.
- Monday and Tuesday practice reports on a short week are often estimated rather than observed. Say so when a status rests on estimates, and wait for the first real report before moving confidence much.
- A player returning from a long absence has an unknown workload even when cleared. Confidence in his role, not just his availability, is what belongs in the call.
- When a starter's game is Monday night and the only cover is a Sunday player, the decision belongs to the Sunday lock. A Monday starter at 60 percent to play is a worse bet than a healthy Sunday flex in most cases, because the failure mode is a zero with no recourse.

## Waiver and free-agent evaluation

Score a candidate on all of these before ranking him against the drop:

- Percent owned and the direction of add and drop trends (is the league moving toward him or away from him, and how fast).
- Season total points and positional rank to date.
- Projected versus actual consistency: the share of weeks his actual score landed near his projection. Consistency is worth real points across a season because it keeps flex and bye decisions boring.
- Role trajectory: snaps, targets, carries, and whether the role is growing, stable, or borrowed from an injured teammate with a return date.
- Schedule: the next three weeks matter more than the rest of season for a streaming add, the reverse for a stash.
- News layer: platform blurbs and beat reporting as inputs, weekly waiver columns as sentiment. If every column leads with a player, expect competition and bid or prioritize accordingly, but let the numbers above decide whether he is worth having.

The drop is half the move. State who goes, why he is the one, and what it costs if the add busts. On a roster with no injured reserve slot, an injured stash occupies a live bench spot, and that cost belongs in the write-up.

### The same-day rule

A target identified today gets acted on or surfaced today. The failure this rule exists to prevent: a strong streaming defense is identified on Wednesday morning, the action is parked behind a weekend reminder, and a league-mate claims the defense on Wednesday at noon. Free agents clear on the league's schedule, not on the assistant's reminder schedule.

### Waiver mechanics change the strategy

- **Rolling priority:** every successful claim costs priority. Spend it on season-changing players, be pickier with one-week rentals.
- **Weekly reset to inverse standings:** priority is free each week. File aggressive claims every week, including speculative ones.
- **Move to last, never reset:** claims are permanently expensive early. Once priority is already spent down, the marginal cost of further claims is low, and the strategy flips to volume.
- **FAAB:** price players against the remaining budget and the weeks left, and never let a column's hype set the bid.

Always confirm the mechanics and any acquisition limits live before applying this. Limits are the settings value most often misreported.

## Defense and special teams

Maintain the standing all-32 board (template in `templates/dst-board.md`), refreshed Tuesdays. For each unit weigh:

- Season total points and the shape of the weekly scores (a unit with a high floor and two spike weeks outranks a pure boom or bust unit of equal total).
- Upcoming matchup, meaning the opponent's offensive points per game, the opponent's tendency to allow defensive points (sacks taken, turnovers given), and likely game script.
- Sack and turnover opportunity as its own line, since those are the scoring events that survive a bad points-allowed day.

Rules:

- Matchup is context, never the whole case. A top-five season unit in a mediocre matchup usually outranks a bottom-ten unit in a dream matchup.
- Prefer holding a two-defense platoon with offset byes and complementary schedules over streaming, when the bench can afford it.
- When a top-tier unit is dropped for its bye week, treat it as a pounce target the same day.

## Kickers

Kickers are the closest thing to a coin flip on the roster. Prefer dome and weather-safe games, offenses that stall in the red zone, and season accuracy over last week's points. Never spend waiver priority on a kicker when a comparable one is a free agent.

## The Tuesday grading rubric

For each contested call of the finished week, record:

- The call and the confidence attached at the time.
- The outcome, in points and in matchup effect.
- A process grade and an outcome grade, separately. Process asks whether the call was right given the inputs at lock time. Outcome asks what happened.
- Bench-beat-starter check: any bench player who outscored a starter at his position, and whether his score was predictable from role, matchup, or news available before lock.

Two failures of the same kind rewrite the framework that produced them. One failure is a note.
