# Decision frameworks

The detailed evaluation logic behind the calls in SKILL.md. Every framework ends in a confidence number from 0 to 100.

## Lineup decisions (start or sit)

Weigh three inputs together:

1. **Projection.** The platform's projection for this week, in this league's scoring. Projections are the starting point, not the answer.
2. **Past production.** The player's actual weekly scores this season, with the trend weighted more than the average. A player whose last three weeks beat his season average is a different asset than one fading the other way.
3. **Expected performance.** A forward estimate built from schedule strength, teammate injuries, role changes, and usage. Examples of adjustments that move this number: a receiver whose team's top option is out (target share up), a running back whose backfield mate is limited (snap share up, or committee risk up), a quarterback facing a defense that funnels passing volume.

House rules:

- Never bench a proven producer on a small projection gap alone. Under roughly two points, start the track record.
- A triggered swap re-opens every slot the involved players can fill. Work the combination, not the pair. The canonical failure: a bench running back's projection jumps on starter-injury news (9.4 to 16.4), so he is swapped straight into the flex over the incumbent flex receiver (13.0) — while a 7.9-point receiver starts untouched at WR2. The right combination was the back at flex and the displaced receiver at WR2, benching the 7.9-point receiver, worth roughly five projected points more than the executed swap. Whenever a bench player's projection jumps into the starting range, rank every starter and bench player who can fill the linked slots (WR + W/R/T, RB + W/R/T, TE + W/R/T) as one pool and start the best combination.
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

### The fresh-grade rule for drops

Never drop a player on an evaluation made before his most recent game — and never on a slice of the season, early or recent. Before any drop, read the candidate's whole season: every game's points and usage. Then split the log where it inflects and diagnose the split. If the recent games differ from the earlier ones, name the mechanism — snaps and touches, red-zone work, a teammate's injury or return, a scheme or role change, schedule and game script — and decide which side of the split describes the player now. Recent form with a mechanical cause behind it is the player's present level; recent form with no cause is variance sitting on the baseline. A three-game hot streak proves nothing by itself, and a three-game slump buries nothing by itself; the why is the evidence. If the whole-season read cannot be written from current data, the drop does not happen yet.

The failure this rule exists to prevent: a committee back is graded the bench's weakest player in early October, off two quiet weeks (2.5 and 2.6 points). Three weeks later he is dropped to make room for a handcuff stash — on that same early-October grade, never re-derived. The whole-season read would have stopped it twice over. First, the grade was three games stale: he had since scored 16.2, 14.0, and 17.1, and scored again the week after the drop, a fourth straight boom week. Second, the divergence had a mechanism: his per-game efficiency had never dipped (he averaged close to five yards a carry even in the quiet weeks — the slump was volume, not quality), and from mid-October his touches climbed 8, 11, 18, his snap share reached the mid-40s, and his red-zone carries jumped from three in six weeks to six in one game. That is a role expansion, not a hot streak, and it was visible in the game logs before the drop. The add's logic (a handcuff for a star returning from bye) was defensible on its own; the drop was executed on a partial-season verdict whose own data had already refuted it. A standing grade is a hypothesis with an expiry date: the player's next game.

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
