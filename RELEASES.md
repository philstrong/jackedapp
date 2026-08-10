# Jacked — Release Notes

## Build 248 (v1.4.8 — August 10, 2026)

**Tap the medal on a workout in History and its finish summary comes back — your totals, your wins, and your coach's read on the session.**

The recap you get when you wrap up a workout used to be a one-time thing: scroll past it and it was gone. Now each of your recent sessions carries a small medal button that reopens it, put together from what's already on your phone — no waiting on a connection, no coach call. It reads the numbers as they stood that day, so a PR you set a few weeks back still shows up as a PR instead of getting buried by everything you've done since. Your coach's write-up gets saved with the session from here on out too, including when you hit Done while it's still typing — which used to lose it — so workouts from before this build will show your stats and wins but not the prose. The offline notice is quieter as well: the red bar and the floating pill are gone, replaced by a line in your coach's status area and a nudge in the chat box that you can keep logging by hand.

---

## Build 246 (v1.4.8 — August 10, 2026)

**Reports in the Coaching tab come up right away now, instead of holding the whole screen behind a spinner while it waits on the network.**

Your plan cards are worked out from what's already on your phone, but the pane was waiting on the report list to come down before it drew any of them — so on a slow signal you'd sit looking at a spinner with everything it needed already sitting there. Now the cards come straight up, and each one's report line fills in on its own as it arrives, with a soft placeholder holding the spot until then. The placeholder only shows on the first load of the day, so generating a new report doesn't flash the cards you've already got back to empty.

---

## Build 245 (v1.4.8 — August 9, 2026)

**Opening the app without a signal no longer kicks you out to the sign-up screen — you stay logged in and can keep logging your workout.**

If your session had gone stale and the app couldn't reach the network to renew it — a basement gym, a dead spot, airplane mode — it read that as "signed out" and dropped you on the sign-up screen with a workout in progress. Now it keeps you signed in and switches to manual logging: a small "Offline — Coach paused" pill up top, and the chat box points you at logging sets by hand instead. Everything you log while you're out there saves locally, and the moment you're back on a signal it syncs up and your coach comes back. Only a genuine sign-out sends you to the auth screen now, and a flaky connection can never wipe your login on its own. The suggested weight on an exercise row got two fixes as well: it no longer sits there showing an old number when your coach has already moved you to a different weight, and it stops picking a months-old session as your "last time" — an older workout that got edited or re-synced could jump to the front of the line and drag the suggestion down with it. And when you go back and hand-correct a past workout in History, your coach now knows you corrected it and trusts those numbers over what it remembers from the conversation.

**The target on an exercise row now agrees with your coach, instead of sitting there with a different weight than the one in the chat.**

Each lift in your session list carries a little target worked out from your history, and it had no idea when your coach had moved you somewhere else — so the row could read 100 lb while the spec line, the input bar and the chat had all moved on to 147.5. Now, when your coach makes a concrete call on a lift, the row defers to it instead of showing a competing number. The history those targets come from was being read in the wrong order too: if an older workout got edited, or came back down from a sync, it could be treated as your most recent day for that lift — so the suggestion was built off a session from weeks ago instead of the one you just did. If you've gone back and hand-fixed a past workout in History, your coach now knows it was corrected and trusts what's stored over what it remembers from the chat. And the reports in the Coaching tab no longer sit behind a full-screen spinner — your plan cards come straight up from what's already on your phone, with each report's line filling in as it arrives.

---

## Build 244 (v1.4.8 — August 7, 2026)

**The set editor got rebuilt around one number at a time — a stepper, quick jump sizes, and a keypad when you'd rather just type it — and it's now what opens everywhere you edit a set.**

Instead of the old two-column keypad, tapping a number opens a card right above the chat box with that field already selected: a big value, minus and plus on either side, and a row of jump sizes underneath — reps by 1, 2 or 5, weight by 2.5 up to 45 — so going from 135 to 185 is a couple of taps. Tap the value itself and the keypad drops in if you'd rather type it outright, and tapping anywhere outside puts the editor away. Each field has a small × to clear it back to zero, and on a lift you'd normally do with just your bodyweight, a cleared weight reads "BW" instead of 0. The same editor now covers all three places you'd change a set — a logged card mid-session, a set you're adding by hand, and going back to fix a workout from History — and backing out with unsaved changes asks before it throws them away. Adding a set to a lift got two fixes too: the controls now come up in the shape of the exercise you're actually on, seeded with what you just did this session rather than last week's target, and the extra set properly shows up as a pending bubble instead of quietly doing nothing. The collapsed workout card at the top of Train is slimmer as well, which hands a bit more of the screen back to the chat. And if you're in early access, the app has moved to five tabs with Train raised in the middle, and your coach reports and coach memory now live together under a new Coaching tab instead of being tucked inside History.

---

## Build 243 (v1.4.8 — August 5, 2026)

**Tap-to-log got real controls — nudge the reps or the weight right above the chat box, then hit the check to log the set.**

For anything you count in reps, the row of suggested rep buttons has been replaced with a compact set of controls sitting just above where you type: minus/plus on the reps, your weight beside them, and a green check to log it. It starts on whatever your coach prescribed, so hitting the number exactly is still a single tap — but if you squeezed out an extra rep or went up five pounds, you can dial it in first instead of typing out a message. Tap either number and the full-size editor opens with those values already in it; saving from there logs the set exactly the same way, coach reply and all. Bodyweight moves show reps only, and timed and cardio work keeps its old buttons for now. The sheet you get when you finish a workout was rebuilt too — a proper little celebration, your totals counting up next to how they stacked against last time, your wins for the session, and your coach's read on it along with what it's lining up for you next.

---

## Build 242 (v1.4.7 — July 30, 2026)

**When your coach moves you to the next lift, the "you're here" marker moves with it — instead of staying parked on one you only glanced at.**

A few builds back, tapping an exercise started moving the pointer instantly, without waiting on your coach. The catch was that an old tap could outrank a newer instruction: if you peeked at squats mid-session and your coach then moved you on to RDLs, the header could sit on "Squat, set 2 of 3" while the chat, the tap-to-log chips, and everything getting logged had all correctly moved to RDLs. It only straightened itself out once your next set landed. Now a fresh move from your coach clears the stale tap so it all points at the same lift, and tapping still jumps you there right away, same as before. Your coach also got better at bodyweight moves — pull-ups, dips and the like no longer come back with a meaningless "0 lb" to hit, just a rep target, which also stops the previous exercise's rep count from tagging along.

---

## Build 241 (v1.4.7 — July 30, 2026)

**Adding an exercise mid-workout no longer crashes the app.**

Since the last couple of builds, the session list has been rearranging itself as you work — lifting the exercise you tapped up the tree, sliding finished ones into the order you did them. The rows were gliding into their new spots, and that glide was crashing the app outright when a row got added or moved at the wrong moment. Adding an exercise to a live session was the easiest way to hit it. The animation is gone for now, so the list snaps into its new order instead of sliding — everything still reorders exactly the same way, it just moves in one step. We'll bring the glide back once it's built on something that won't take the app down with it.

---

## Build 240 (v1.4.7 — July 30, 2026)

**Lifts you've finished now sit in the order you actually did them, so your session list and your history tell the same story.**

If you worked your plan out of order — Arnold press before bench, say — the finished part of the session list still snapped back to the order the plan had them in. So Train read "Bench, Arnold" while your history read "Arnold, Bench" for the same workout, which made it hard to tell what you'd actually already done. Now a finished lift stays where you did it, top to bottom in completion order, matching what you see in History. Anything you haven't started yet still sits in plan order, waiting for you.

---

## Build 239 (v1.4.7 — July 30, 2026)

**Tapping ahead to another exercise now moves you there instantly, instead of waiting on your coach to catch up.**

Last build let you skip to a different lift when a machine was taken, and the session list reordered to follow you. But the "you're here" marker and the tap-to-log chips above the chat box stayed parked on the lift you'd just left until your coach's reply came back — so for a second or two you'd be looking at the new exercise with the old one's rep buttons underneath it. Now the tap moves all of it at once: the pointer, the chips, and the list. Your coach catches up a moment later and picks up its prescribed reps and weight from there, same as before.

---

## Build 238 (v1.4.7 — July 29, 2026)

**Skip ahead when a machine's taken and the session list reorders to follow you — so your coach stops calling the workout done while you've still got lifts left.**

If the bench was busy and you jumped to the last thing on your plan, the list stayed in its original order, and your coach saw you at the bottom of it and wrapped the session up — even though the bench was still waiting for you. Now tapping an exercise lifts it up the tree right away, so the list reads top to bottom as what you've finished, what you're part-way through, what you're on now, and what's left, with the rows gliding into place instead of jumping. Your coach reads that same list, so anything you moved past is still sitting there and it keeps working through it with you. Two coaching fixes came along too: logging a warmup no longer makes your coach restart the count and ask for an extra set at the end of a lift (warmups still stay out of your progression), and if you call out the weight in one message and the reps in the next, that weight stays on the set instead of getting dropped.

---

## Build 237 (v1.4.7 — July 28, 2026)

**The rest timer now chimes when you're logging on your own, not just in a coached session.**

If you were tap-logging your sets and left the phone sitting face-up on the bench, the rest timer would run out in silence — no chime, no buzz. It only ever rang if you'd locked the phone or switched apps, or if you were in a coached session. Now the bell and the haptic fire in both modes with the app open, and it still skips the in-app chime when your phone already dinged you in the background, so you don't get hit twice for the same rest.

---

## Build 236 (v1.4.7 — July 28, 2026)

**The "how to log this" hint in the chat box is short enough to actually read now — and a one-mile walk no longer reads "1 miles."**

For the moves with no tap-to-log chips — a walk, a run, a plank, a carry — the chat box shows you what to say to log it. It used to read "Log 20 min · 1 miles or message Kelly…", which was longer than the one-line box, so the end of it got cut off. Now it's just "hint: 10:15 1 mi" — the time in clock form, a short unit, and it fits. The "1 miles" slip is fixed everywhere else it showed up too, so a one-mile walk reads "1 mile" on your history and session cards and in the edit sheet.

---

## Build 235 (v1.4.7 — July 27, 2026)

**When you move to a new lift and just call out reps, the app no longer fills in a weight you never said.**

If you finished leg press at 200 and then said "10 reps" on the leg extension, your set could land in the log at 200 lb — the weight carried over from the lift you'd just done, on a machine you hadn't put a number to yet. It only happened on a brand-new exercise where nothing had been logged and your coach hadn't set a target, but when it did, it quietly wrote a number you never gave it. Now the app leaves that weight blank instead of guessing, so you can fill it in yourself and your totals stay honest. The rest of this build is behind the scenes — every event we log now carries the app version it came from, so we can tell whether a fix has actually reached you.

---

## Build 234 (v1.4.7 — July 26, 2026)

**Every pop-up card in the app now closes the same way — flick it down, tap the dimmed area behind it, or reach for the X in the corner.**

Last build gave the end-of-workout recap a swipe-down and an X; this build takes that everywhere else. The workout picker, the rest-timer explainer, your history stat cards, the milestone list, the coach picker, add-a-plan, your display name, sign-out and delete-account all behave the same way now — and the ones holding more than fits on screen, like the recap and your full milestone list, actually scroll instead of sitting stuck. The rest-timer explainer also got a little smarter: it's now reachable when you're logging on your own, not just in a coached session, and it only opens when a timer is genuinely counting down instead of any time you tapped that row. A few smaller things came along too — tapping the "lb" next to a number no longer flips you to kilos mid-log (that choice lives in Settings), lowering a weight you'd already logged now updates its PR badge instead of leaving a stale one, and for a cardio, plank, or carry — the moves with no tap-to-log chips — the chat box shows you how to log it, like "Log 27:00 · 1.5 mi." And an edit you make to a session you're still in the middle of now gets timestamped properly, so a background backup can't quietly roll it back.

---

## Build 233 (v1.4.7 — July 25, 2026)

**The recap card you get at the end of a workout now closes with a swipe or a corner X — and your coach picked up a run of fixes that make it sharper from the very first message of a session.**

The recap card that slides up when you finish a workout used to strand you if its Done button sat below the fold — there was no way to swipe it away and no X to reach for. Now you can flick it down, tap the dimmed area behind it, or hit an X pinned to the top corner that never scrolls out of sight. On the coaching side, a session sometimes opened with your coach not actually holding your profile — it was getting quietly dropped on the way in, so that first reply could read a little generic; now your coach starts every session knowing who it's talking to. A couple of conversation fixes came along too: when you log a walk or run, your coach takes whatever you give it — distance or time — as a complete report instead of nagging for the part you left out, and before it asks what weight you're starting a lift at, it checks your history first so it can pick up where you left off. And importing a workout history no longer risks colliding with a background backup, so nothing you bring in — or already had — can slip through the cracks in the shuffle.

---

## Build 232 (v1.4.7 — July 24, 2026)

**Finishing a coached workout now brings up the same recap card you get when you log on your own — and every completed session in your history shows its total volume.**

When you wrapped up a coached session, your coach read you a recap in the chat and that was it — the recap card with your stats, your wins, your coach's read, and a link to your progress report only appeared when you logged a session yourself. Now both kinds of finish open the same card, and the coach's read streams into your Train chat at the same time either way. We also added a total-volume number to each completed session on the History screen — it sits alongside the exercises, sets, and reps counts at the bottom of the card and folds in your body weight the same way the finish recap does. Cardio-only sessions, which have no volume to show, simply leave it off.

---

## Build 231 (v1.4.7 — July 24, 2026)

**The bodyweight work we added last build now counts and reads right everywhere — and finishing your lifts out of order no longer ends your session early.**

Last build gave pull-ups, push-ups, and dips real volume, but a couple of gaps slipped through: when you logged on your own, the "add your weight" prompt sometimes didn't appear and those sets still counted as nothing, and in a few spots a bodyweight set showed up as a broken "18 × 0 lb." Both are fixed — bodyweight sets now read as plain reps ("18 reps") on the Train screen, in your history, and in your coach's wrap-up, and they count toward your total no matter how you log them. Your coach's end-of-session recap now folds that body weight into the total too, so it can't headline "volume up" on the card and then talk past it. And if a machine's taken and you finish a later lift before an earlier one, the app no longer calls the whole session done — the rest timer stays put, the "session complete" banner holds off until you've actually worked through what's left, and logging that last set clears it.

---

## Build 230 (v1.4.7 — July 22, 2026)

**Pull-ups, push-ups, and dips finally count toward your volume — and your coach stops telling you you've finished a walk you haven't started.**

Bodyweight movements used to score zero volume, because there was no weight on the bar — so a session full of pull-ups looked like you'd barely lifted. Now your own body weight counts toward the total, and if we don't have your weight on file yet, a small prompt appears on the Train screen the first time you log a bodyweight set. Whatever you enter gets pinned to each session as you finish it, so past workouts keep their numbers even as your weight changes. Your coach also picked up three fixes from a read-through of a few weeks of real conversations: it no longer treats a walk or run you haven't started as already done, it reads back the weight and reps you actually called out instead of the ones it prescribed, and it stops re-announcing a lift from the top every time you circle back to it. And editing a logged workout — adding an exercise, deleting a set — no longer snaps back to the old version if a background sync happens to land at the same moment.

---

## Build 229 (v1.4.6 — July 21, 2026)

**A quiet maintenance build — some behind-the-scenes tidying, nothing new to spot up front.**

No new features in this one. We did some housekeeping under the hood so walks, runs, and other cardio are counted properly alongside your lifts. Everything you'd notice is already in place from build 228 — keep logging and training exactly as you did before.

---

## Build 228 (v1.4.6 — July 21, 2026)

**You can now add a lift to a session straight from the list of exercises on your screen — in coached sessions too, not just when you're tapping through it yourself.**

If a machine's taken or you just feel like throwing in an extra lift, there's now an "Add exercise" row at the bottom of your session's exercise list. It shows up whether your coach is running the session or you're logging it yourself — coached sessions had no way to add anything before, and when logging on your own it sat off on its own row under the lift you were on. Your coach picks up the addition on its own, so you don't have to say anything. And if you change your mind before you've started that new lift, the × next to it now takes it off the list entirely instead of leaving it struck through as skipped — lifts that were in your plan to begin with still get the old skip treatment.

---

## Build 227 (v1.4.6 — July 20, 2026)

**Your Profile tab is now two tidy pages — one for you and your coach, one for all your settings — with a single tap in the corner to flip between them.**

The Profile tab used to be one long scroll that mixed who you are in with every setting in the app. This build splits it: a little person-and-cog toggle up top flips between a Profile page — your name, your coach, and a single card holding your workout count, week streak, and average session time (each still taps to explain itself), plus your milestones — and a Settings page that gathers everything else in one place: units, the rest-timer bell, haptics, weight increments, import and export, and sign-out. Switching coaches now opens a clean pop-up picker instead of a row of tiles. We also put each plan's muscle focus right on the Plans list — "arms, chest, shoulders" reads on the row the same way it does on the workout cards, and groups like "full body" now show in plain words instead of a code-ish "fullBody." And two coaching fixes from live testing: your coach now reads the exact route on your screen, so it no longer loses track of which set you're on, and you can tap back to a lift you already finished to add one more set mid-session — your coach counts the extra instead of calling the exercise done.

---

## Build 226 (v1.4.6 — July 19, 2026)

**The progress charts got a proper clean-up — real dates along the bottom, your best number called out up top, and long histories you can scroll back through.**

The charts on your Progress tab now label the bottom edge with actual dates, so you can see when a session happened instead of counting across from the end. Your best number for a lift is pinned at the top of the chart so the ceiling is always readable, and the horizontal guide lines now land on plate-real numbers — 2.5, 5, 10 — instead of whatever the math happened to land on. Pull-ups, dips, and the like now chart your reps rather than a weight, and the machine-assisted versions show the assist as a negative so more help reads as less progress. And once a lift has enough sessions to get crowded, its chart scrolls sideways: it opens on your latest session and you can drag back through the history, with the numbers up the left side staying put while the chart slides underneath.

---

## Build 225 (v1.4.6 — July 18, 2026)

**A shaky connection at the wrong moment — like right as you finish a workout — no longer lets a stray "network request failed" error slip through.**

Jacked fires off a couple of quiet background requests as you use the app — one to note what you did, one to keep your profile up to date — and neither is meant to bother you if it can't get through. A weak signal at the wrong moment used to let one of those surface as an error instead of failing silently. This build makes them fail quietly the way they always should have, so a dropped connection while you're wrapping up a session stays out of your way.

---

## Build 224 (v1.4.5 — July 18, 2026)

**A workout you log with no signal now backs itself up on its own the moment you're back online, instead of waiting around for the next sync.**

Logging a workout has always worked with no connection — you can run and record a whole session offline. The catch was that if the upload happened to fail while you were out of range, that session just sat on your phone until something else synced it later. This build makes it retry on its own: as soon as your connection returns, or you reopen the app, any session that didn't make it up gets backed up automatically. And it does so safely — a workout you logged on another device while this one was offline won't get overwritten in the process.

---

## Build 223 (v1.4.5 — July 18, 2026)

**The coaching preview that slides up when you reach for the coach can now be swiped down to close, the same way you close the Choose Workout sheet.**

When you head toward coaching without a subscription, a preview slides up showing what your coach unlocks. Until now you closed it with the button on the sheet — this build lets you just flick it down with your finger, matching the gesture we added to the Choose Workout sheet last build. Drag it partway and let go and it springs back, pull it past halfway and it slides the rest of the way closed. Every button on the preview still works as before — the subscribe call, "see all," "keep it free," and the legal links all stay tappable.

---

## Build 222 (v1.4.5 — July 18, 2026)

**You can now swipe the Choose Workout sheet down to close it, instead of hunting for the little X.**

When you go to start a session, the Choose Workout sheet slides up over your screen. Until now the only way out was the X in the corner. This build lets you just flick the sheet down with your finger to dismiss it — drag it partway and let go and it springs back, pull it past halfway and it slides the rest of the way closed. The plan list underneath still scrolls normally, and the X, import, and settings buttons all still work as before.

---

## Build 220 (v1.4.5 — July 17, 2026)

**When you log on your own without a subscription and slide the session over to your coach, you now get the same gentle preview of what coaching offers instead of jumping straight to the full subscription screen.**

If you tap through your workouts yourself, there's a slide control that hands the session over to your coach. Completing that swipe used to drop you straight onto the full subscription screen — even though the coach-mode switch right next to it showed a softer preview of what coaching unlocks. Now both behave the same way: sliding over shows that same gentle preview, so the hand-off feels consistent however you reach for it.

---

## Build 219 (v1.4.5 — July 17, 2026)

**You can now tell Jacked how much the weights at your gym actually jump, so a heavier next-time target matches your dumbbells or machine stack instead of always assuming five pounds.**

Until now, when Jacked bumped your target for next time it always stepped up by five pounds — but that's not how every gym works. Some dumbbells go up in 2.5s, a machine stack might jump ten. There's a new "Weight increments" section in Settings with two pickers, one for free weights and one for machines and cables, and whatever you pick is the size of step Jacked uses when it nudges a target up or eases one off. It defaults to five, so nothing changes unless you go set it. We also fixed up progress reports: the report you tap into now scrolls properly, so you can read the whole thing and reach your earlier reports underneath, and when a plan isn't ready for a fresh report yet it now always tells you exactly how many more sessions to log.

---

## Build 218 (v1.4.5 — July 17, 2026)

**Logging a workout by tapping through your sets is out of early access — it's now free for everyone.**

Up to now, tapping through a workout to log it yourself was an early-access feature. This build opens it to everyone at no cost: pick "tap it yourself" in the logger and you can run and record a whole session without a subscription. Coaching — your coach walking you through a session, your written progress reports, and the coach remembering your history across sessions — is what a subscription now unlocks. We also cleaned up a handful of things along the way: when your coach is targeting a heavier weight next time, the one-tap prefill now offers that new number instead of quietly repeating your last one, so tapping it doesn't miss the bump; beating last time's reps at the same weight now shows up as progress on your logged set; the mid-session "View plan" peek shows your targets (or the right lock) correctly again; an edited session's duration is capped at a sensible three hours instead of running to absurd values; and the "ready to try" nudge that had been silently failing to send now actually reaches people.

---

## Build 217 (v1.4.5 — July 15, 2026)

**Every next-time weight target picked up a tappable coach call — a little pill that has Jack or Kelly explain, in their own voice, why a lift is stepping up or easing off.**

Wherever Jacked shows a target — on the logging screen and in your plan — you'll now see a small pill next to any lift with a call: green when the weight's going up, orange when it's easing off, nothing when you're holding steady. Tap it and your coach talks you through the call in their own voice, built from the actual numbers you've been lifting. The target itself is now a Pro feature — paid members see the number, and free members get a lock that opens an upsell showing how many of today's lifts have a weight call waiting. We also tidied up editing a past workout: its date, start time, and duration are now three separate taps instead of one crowded screen with the number pad always up, and the date/time picker finally closes when you're done with it.

---

## Build 216 (v1.4.5 — July 14, 2026)

**The automatic next-time weight bump isn't locked to coached sessions anymore — tap through a workout yourself and your targets can still step up.**

Last build we tied the automatic weight bump to coached sessions: your coach walking you through a workout would nudge the weight up, but tap through one yourself and your next target just repeated what you last hit. This build lifts that restriction — progression now follows your plan rather than how you happened to log. So when you've earned a heavier target, you get it whether your coach ran the session or you tapped through it on your own.

---

## Build 215 (v1.4.5 — July 13, 2026)

**The automatic next-time weight bump we added last build now only kicks in when your coach is running the session — tap through a workout on your own and your target just mirrors what you last did.**

Last build Jacked started setting a target for your next session — nudge the weight up, hold steady, or ease off — and writing it straight into your plan. This build settles who gets the automatic bump: it's a coached thing. When your coach walks you through a session, the weight still steps up once you've earned it; when you tap-log a workout yourself, your next target simply repeats what you last hit instead of pushing the number up on its own. We also cleaned up a small edge case — a weighted move you'd logged without actually punching in a weight could show a nonsense rep target, and now it just leaves the target blank instead.

---

## Build 214 (v1.4.5 — July 13, 2026)

**When you finish a workout, Jacked now sets your target for next time — a little heavier, hold steady, or back off — and saves it right into your plan, so each move shows what you last did and what you're aiming for.**

Finish a strength session and Jacked looks at what you just lifted and works out where each move should go next time — nudge the weight up, keep it where it is, or ease off — then writes that target straight into your plan. Open the plan and every move now shows a "Last … · Target …" line, so you can see at a glance what you hit last session and what you're chasing next. The number comes from the same progression logic the app already uses, not a guess. We also tidied up a few early-access corners: finishing a tap-to-log workout without logging a single set no longer saves a blank session or pops a recap — it just steps aside — your progress reports now weigh a move's full history when they spot trends, and when there's nothing worth reporting yet you get a proper explainer instead of a line of red text. The coached-versus-tap-it-yourself switch also picked up a clearer hand-tap icon.

---

## Build 213 (v1.4.5 — July 11, 2026)

**The tap-to-log screen got a design pass — a cleaner switch between having your coach walk you through a session and tapping through it yourself, clearer icons in your list of moves, and little pencils that show exactly where to tap to fix a set.**

If you're in early access and log by tapping your sets, this build tidies up how the whole thing looks. Picking between a coached session and tapping through it yourself is now a simple side-by-side toggle, your list of moves picked up small icons so each one's easier to spot at a glance, and every value you've logged shows a tiny pencil next to it — including the empty placeholder rows for sets you haven't filled in yet — so it's obvious you can tap to change it. We also cleaned up a few smaller things: timed moves now keep their seconds instead of rounding off, an exercise you tap back to revisit stays marked as done rather than flipping to "current," and cardio set counts read from your last session properly. And there are six new tips sprinkled through the app pointing out things like tap-to-log, set tags, importing your history, and the progress charts.

---

## Build 212 (v1.4.5 — July 10, 2026)

**One more tidy-up on the workout wrap-up — each big stat number now sits centered in its card instead of hugging the left edge.**

If you're in early access and log by tapping your sets, this is a tiny cosmetic touch to the finish recap. The three stat cards were already lined up neatly, but the Volume, sets, and duration numbers themselves were pinned to the left. Now each one sits centered under its label, so the whole row reads balanced. Nothing about how you log or train changed.

---

## Build 211 (v1.4.5 — July 10, 2026)

**A couple of fixes for tap-to-log: your expanded list of moves stays visible, and the rest countdown moves off the session clock so both are readable again.**

If you're in early access and log by tapping your sets, this build sorts out two rough edges from the last few updates. The fold-up animation we added a couple builds back could leave your list of moves blank after it collapsed — it would tuck away fine but come back empty when you opened it again — so we've pulled the animation out and the list snaps open and closed reliably like it used to. And the rest countdown between sets, which had been sitting at the top of your workout card in place of the session clock, now shows down by the chat bar instead — the same spot it uses when you're being coached — so your session clock is back in the header where it belongs.

---

## Build 210 (v1.4.5 — July 10, 2026)

**Once you've moved on to the next exercise, you can tap a finished one to go back and fix a set you already logged.**

If you're in early access and log by tapping your sets, this fixes going back. Before, once you logged a set and the workout moved you on to the next exercise, the one you just finished was locked — you couldn't tap it to check or fix what you'd entered. Now a completed exercise is tappable again: tap it and it reselects, your logged sets show back up, and you can tap any set to edit it. Coaching works exactly as before.

---

## Build 209 (v1.4.5 — July 10, 2026)

**When your workout list closes back up, it now folds down into the card instead of fading away in place.**

A small animation touch-up. When you've got your list of moves expanded and it collapses — whether you tap the chevron, tap away, or let it settle on its own — the timeline now folds up vertically into the collapsed card rather than fading out where it sits. It reads as one piece tucking away instead of two things happening at once. Nothing about how you log or train changed; it just moves a little more naturally.

---

## Build 208 (v1.4.5 — July 10, 2026)

**The wrap-up you get after a tapped-through workout is a touch tidier — the three stat cards line up cleanly and a big Volume number reads as something like 12.3K instead of running long.**

If you're in early access and log by tapping your sets, the finish recap got a small cosmetic polish. The Volume, sets, and duration cards now sit on the same line no matter how wide each number is, so their labels all line up instead of one drifting down a row. And a hefty Volume total gets shortened — 12,345 shows as **12.3K** — so the three numbers stay compact and evenly sized. Nothing about how you log changed; it just looks neater.

---

## Build 207 (v1.4.5 — July 10, 2026)

**Logging a timed move now works like a stopwatch — punch in minutes and seconds instead of just whole minutes — and your progress report closes with a tap outside it.**

When you log something measured by time — a run, a carry, a timed hold — the number pad now reads as **MM:SS**, so a 10-minute-34-second effort goes in as `10:34` instead of rounding off to whole minutes. Type the digits like a stopwatch and they fill in from the right; the plus and minus buttons still nudge a minute at a time without touching your seconds. And if you're in early access and pop open a progress report, you can now tap anywhere outside it to close it, the same as the app's other sheets.

---

## Build 206 (v1.4.5 — July 9, 2026)

**Setting when a workout happened is tidier now — the same date and time picker shows up whether you're logging one by hand or fixing a past session, and neither will let you pick a time that hasn't happened yet.**

When you set the date and start time for a workout — logging one yourself or editing an old session in History — you now get the same native calendar and time spinner in both places, instead of two different pickers. Manual logging drops its old shortlist of "yesterday / two days ago" shortcuts and rough time chips for that same calendar, so landing on an exact day and time is easier. And both pickers now stop at the current moment, so you can't accidentally set a workout for later today or some day down the road.

---

## Build 205 (v1.4.5 — July 9, 2026)

**A few finishing touches for tap-to-log — your workout list now slides open and closed instead of snapping, the rest countdown shows while you log, and each set's "last time" hint lines up set by set.**

If you're in early access and log by tapping your sets, this build smooths out a handful of rough edges. Your workout list now animates open and closed however it collapses — tapping the chevron, tapping away, or letting it settle on its own — instead of jumping. The rest timer between sets now shows its countdown right at the top of your workout card while you tap-log, the same way it does when you're coached. And the faint "last time" hint on each row now mirrors exactly what you did set by set — warm-ups included — so a heavier opener and a lighter back-off set each show their own reps and weight instead of one flat number.

---

## Build 204 (v1.4.5 — July 9, 2026)

**A quiet maintenance build — a little behind-the-scenes tidying, nothing new to spot up front.**

No new features in this one. We did some housekeeping under the hood so switching between how you log and train stays smooth and predictable. Keep logging and training exactly as you did before.

---

## Build 203 (v1.4.5 — July 8, 2026)

**Tapping a different move in your workout now takes you straight to logging it, and adding a set no longer bumps you off the one you're on.**

If you're in early access and log by tapping your sets, this one smooths out jumping around your workout. Before, tapping another move in your list could highlight it without actually switching what you're logging — or switch it without moving the highlight — so the two could drift out of step. Now they move together every time: tap any move and it lights up and is ready to log in one go. And tacking on an extra set with the **+** just adds the set, instead of quietly yanking you back to a different lift.

---

## Build 202 (v1.4.5 — July 8, 2026)

**Log by tapping? It now works a lot more like being coached — a rest timer between sets, an automatic hop to your next lift, and no more crash when you tap Finish.**

If you're in early access and log by tapping your sets, this build closes a bunch of the gaps between tap-logging and being coached. Logging a set now kicks off the same two-minute rest timer your coach uses — the countdown shows right on your workout card and buzzes you when it's up — and once you've wrapped a move, Jacked walks you straight on to the next one you haven't done yet instead of jumping back up the list. There's a little **+** next to whatever you're logging to tack on an extra set, tapping a set you already logged now edits it in place instead of leaving a duplicate, and reps-only moves like pull-ups stop asking you for a weight. We also lined up how many sets tap-logging plans for you with what your coach would pick, so the two always agree, gave the finish recap a cleaner layout that can hand your session straight to your coach, and squashed a crash that was hitting about one in ten workouts right as you tapped Finish.

---

## Build 201 (v1.4.5 — July 8, 2026)

**Wrap up a tapped-through workout and the recap now hands you more to celebrate — PRs, a jump in total work, milestones, and always at least one good word.**

If you're in early access and log by tapping your sets, the little wrap-up you get when you hit Finish got a lot warmer. Instead of just your numbers, it now pulls the real wins out of the session — a new weight PR, when you moved more total than the last time you did this same workout, a session milestone you just crossed — and if none of those landed, it still gives you credit for the session and whatever streak you've got going. Your Volume stat spells out its unit now, too (lb or kg), so there's no second-guessing what the number means. A couple of other tap-to-log touches: your workout list stays pinned at the top instead of sliding away as you log, every set you tap in gives a little buzz, and the set it teed up next now mirrors the last one you actually did this session — so it eases off right along with you as you tire.

---

## Build 200 (v1.4.5 — July 7, 2026)

**Two small touch-ups to tap-to-log, so your "last time" numbers and comparisons read just like they do when you're coached.**

If you log by tapping through your sets, the faint "last time" hint on each row now lines up exactly with what your coach shows you — and for any extra sets beyond what you did last session, it repeats that session's final set instead of going blank, so every row has a number to work from. We also cleared out the "= matched" tag that used to pop up whenever a set landed right on last time; now a set only flags a badge when you actually beat it or came up short, keeping the screen calmer.

---

## Build 199 (v1.4.5 — July 7, 2026)

**Tap one of Jacked's reminders and it now drops you straight onto the Train screen, ready to pick up your workout.**

When a nudge from Jacked lands on your phone and you tap it, the app opens right to Train instead of wherever you last left off — so you're one tap from getting started. Behind the scenes we also started keeping track of which reminders actually get you back in the gym, so over time we can send fewer of them and time them better.

---

## Build 198 (v1.4.5 — July 7, 2026)

**In early access, you can now switch between coaching and tap-to-log without leaving your workout — and Jacked remembers which one you prefer.**

Open up any move in your session and you'll spot a little coach switch on the card: leave it on for coached chat, or flip it off to just quietly tap your sets in. You can swap back and forth as much as you like mid-workout — your coach is always one tap away, and so is heads-down tap-logging. Whichever you land on sticks, too: close the app or start a fresh session and Jacked drops you right back into the mode you were using instead of always opening in chat. The Coach / Tap control on the Choose Workout screen now matches that same switch, and the picker sheet settled back to its steadier layout after the previous build's sizing tweaks were nudging the Train screen around.

---

## Build 197 (v1.4.5 — July 6, 2026)

**The Choose Workout screen got a clearer Start button, and if you log by tapping, that mode now sticks around after you close the app.**

We reworked the top of the Choose Workout sheet: there's now one bold Start button that spells out exactly what it'll do — "Start [plan]" when you're heading into coaching, "Log [plan]" when you're tapping through your sets — with the early-access Coach / Tap toggle tucked neatly beside it. The whole sheet is slimmer too, so both rows of your plans stay in view without scrolling, the coach tip scrolls along with them instead of hogging the top, and you can swipe it down to dismiss. If you're logging by tapping and you close the app mid-workout, it now picks back up in tap-to-log mode instead of dropping you into chat. And one fix for tap-to-log: starting a walk or other cardio move you hadn't logged yet was pulling up the reps-and-weight keypad — now it opens the right time-and-distance one.

---

## Build 196 (v1.4.5 — July 6, 2026)

**Prefer tapping to talking? In early access you can now log a whole workout by tapping through your sets, no chat required.**

The Choose Workout screen has a new Coach / Tap-to-log toggle for early-access members. Pick "Tap to log" and you get a full-screen view of your workout laid out set by set — each row shows what you did last time as a faint suggestion, and a single tap logs it and moves you on to the next, calling out how you stacked up as you go. You can slide over to live coaching any time mid-workout, and if you're logging an older session you can set its own date and time; when you wrap up, you get a quick recap of your stats and any personal bests or milestones you hit. We also tucked an Import shortcut into the "log a past workout" sheet on your History tab, so bringing your sessions over from Strong or Hevy is now reachable from one more place.

---

## Build 195 (v1.4.4 — June 30, 2026)

**The recap your coach gives you after you tap Finish now gets your sets — and how they stack up against last time — right.**

Before, that after-workout wrap-up could jumble your numbers or invent a comparison — read back a couple of sets at 135 and a couple at 155 as some other mix, or tell you "bench's up across the board" on a day you'd purposely gone lighter. Now it reads your sets cleanly and only calls out what actually changed since last time, treating a lighter day as the smart deload it is instead of a slip. Your Progress charts got clearer too: your best set now stands out with a dashed ring and always spells out the full weight and reps behind it, with an extra gridline to make the weight scale easier to read. And if you're in early access, the per-plan coaching reports ease up on a lift that's only dipped a little when you've got a long run of sessions behind it — a small step back reads as a minor dip, not an alarm.

---

## Build 194 (v1.4.4 — June 29, 2026)

**Bringing your past workouts over from Strong or Hevy is now open to everyone — and it's easier to find.**

Importing your history used to be an early-access perk; now anyone can do it. If you've got an export from Strong or Hevy, Jacked reads through it and folds those past sessions into your history, so your coach starts out already knowing what you've been lifting. There's a new "Import workout history" button right under "Start your first workout" on the History tab when it's empty, so you can bring everything over before you log your first set — and it's still available any time from Settings.

---

## Build 193 (v1.4.4 — June 29, 2026)

**Importing your history now lets you pick exactly which routines turn into plans — and your Profile milestones are back to showing the full row.**

If you're in early access and bringing your past workouts over from Strong or Hevy, the last step of the import now lays out every routine it spotted as a card you can tap to choose — Jacked pre-picks as many as you have open plan slots for, and if there's one you'd rather have instead, you can free up a slot by removing a plan you're not using right there on the screen. A couple of touches land for everyone too: the Milestones row on your Profile sometimes collapsed into a single oversized bubble, and now it always lays out the full set of six, while your milestone count sticks to this year's workouts so a big history import doesn't quietly inflate it. We also stretched how far back the app holds onto your sessions — from one year to two — so more of what you import stays put.

---

## Build 192 (v1.4.4 — June 28, 2026)

**Two fixes to how your coach reads your sets — it stops calling you done early, and a bare rep reply keeps the weight you were already lifting.**

If you regularly knock out four sets of a move but kept hearing "nice, you're done" at two or three, that's fixed: your coach now goes off the most sets you've done across recent sessions instead of your usual count, so it won't cut you short on the days you've got more in you. And if it ever lines up one set too many, just say "moving on" and it rolls with it. The second fix is about logging — when you'd been pressing a move at 80lb and the coach asked only for reps, firing back a bare "6" used to log that set at zero weight, wiping the 80 off your card and your progress for that lift. Now it carries the weight you were already using on that same move forward, so a quick rep reply logs the full set.

---

## Build 191 (v1.4.4 — June 28, 2026)

**Need one more set than the plan called for? Tap the + on the session map and it drops right into your lineup.**

The slim session-map bar shows a row of dots for the sets you've got planned on your current move — now there's a + sitting right beside them. Tap it and another set slides into your lineup on the spot, so when you've got an extra one in you, you don't have to wrestle the app to log it. We also moved the swap and skip buttons to sit right next to each move's name in the expanded map, and you can now skip the move you're currently on, not just the ones ahead — either way your coach hears about it and picks up on the right exercise. One small fix: cardio distances that used to render as a long tail of decimals (0.6599999…) now show clean, like 0.66.

---

## Build 190 (v1.4.3 — June 27, 2026)

**Swap an upcoming move you haven't started yet for a different exercise, right from your session map.**

In the session map — your workout laid out move-by-move — any move you haven't logged a set on yet now carries a small swap button. Tap it, pick a different exercise, and it takes that move's place in your lineup; the swap sticks even if you close and reopen the app, so when you get there your coach sets you up on the new move just like any other. And if you're in early access, importing your history from Strong or Hevy now goes a step further — Jacked spots the routines you train regularly and offers to turn each one into a plan with a single tap, so you start out with your usual splits already built instead of recreating them by hand.

---

## Build 189 (v1.4.1 — June 26, 2026)

**For early access: bring your history over from Strong or Hevy, so your coach knows your lifts from your very first set.**

If you're in early access, Settings has a new "Import history" row. Point it at a workout export from Strong or Hevy — the CSV file those apps hand you when you export — and Jacked reads through it and folds those past sessions into your history, so your coach starts out already knowing what you've been lifting instead of treating day one like a blank slate. It lines the exercises from the other app up with Jacked's own, and anything it doesn't recognize it adds as a custom move so nothing gets dropped. You'll see a summary of what it found before anything is saved, and if it's not right you can undo the whole import in a single tap.

---

## Build 188 (v1.4.0 — June 26, 2026)

**Your coach now carries what you lifted last time into every message — so it stops treating a move you've already done as brand new partway through a workout.**

Before, your coach only pulled your history for each move at the very start of a session, so if you circled back to a lift later it could act like you'd never logged it — "first time on this one" — even when you had. Now it keeps your last sets for every move in front of it the whole time, so its weight and rep suggestions stay tied to what you've actually done all the way through. Two smaller touches in the session map: walking and other cardio moves now carry a "last time" line with your time, distance, and pace, the same way your lifts do, and skipping a long cardio move — say a 20-minute walk — now drops your time-left by its full length instead of trimming off just a minute or two.

---

## Build 186 (v1.4.0 — June 25, 2026)

**The session map and the Progress view are now open to everyone — plus pace on your cardio and a coach that's easier on your run-and-walk days.**

The move-by-move session map and the Progress view — the charts that show how each of your exercises is trending, with badges for where your coach is steering you — were early-access only until now, and both are open to everyone in this build. We also added pace to your cardio: when a set has both a time and a distance, you'll see your pace (like 6:40/mi) right next to it on the Train card and in your History. Your coach is easier to deal with on cardio days too — after a quick "0.5 mi" it shows you how to log the rest instead of pelting you with follow-up questions — and an empty Progress tab now greets you with example charts so you can see what it does before you've logged a thing. One more fix: backing out of the purchase screen no longer pops a stray "Purchase failed" alert. And if you're in early access, Progress gains per-plan coaching reports — tap the sparkle on any plan with three or more logged sessions and your coach writes up a short read on how it's going, drawn from the same trends as your charts.

---

## Build 185 (v1.4.0 — June 23, 2026)

**Your workout totals — Workouts, Streak, and average time — now live on your Profile, right above your milestones.**

The three summary cards that tally how many workouts you've done, your current streak, and your average session length have moved off the History tab and onto your Profile, sitting just above the Milestones card — tap any of them for the same quick explainer as before. If you're in early access, we also tidied up the rest timer in the session map: the REST label now sits right above the countdown ring and UP NEXT above what's coming, so each label lines up with the thing it describes, and the ring quietly blends into the card while you rest instead of standing off it.

---

## Build 184 (v1.4.0 — June 23, 2026)

**For early access: the expanded session map now tucks itself away — tap anywhere outside it, or just leave it be, and it slides back to a slim bar.**

If you're in early access, the session map — your whole workout laid out move-by-move — no longer waits for you to tap the chevron to close it. Tap anywhere outside the expanded view and it folds back down to its slim card, and if you leave it open without touching it for ten seconds it collapses on its own. Touch it again and that idle countdown resets, so it stays open as long as you're actually using it.

---

## Build 183 (v1.4.0 — June 21, 2026)

**Flag how a set felt — failure, warmup, or clean reps — right from the input bar, and your coach logs it with the rest.**

There's a new tag button next to the message bar: tap it for a quick slide-up menu to mark your set as Failure, Warmup, or Clean. Once you arm a tag, the field and the quick-pick chips take on its color so you can see it's set, an ✕ clears it, and whether you tap a chip or type the set yourself, the tag rides along into your workout notes — then clears once you send. We also tidied up the timed-move chips so the quick time options only show on pure holds like planks, not on cardio like walking or running (which already logs distance on its own). And for early access, the Sessions / Progress / Memory toggle moved up right under the header, with the Workouts / Streak / Avg Time tiles now showing only on Sessions — giving the Progress and Memory views the full screen.

---

## Build 182 (v1.4.0 — June 21, 2026)

**A maintenance build — behind-the-scenes reliability work.**

No user-facing changes in this one. Some under-the-hood hardening to how the app handles sign-in and switching accounts (relevant mainly to internal testing) — so a session stays put and your name and data stay tied to the right account through a switch. Everything you'd notice is already in place from earlier builds. On to the next.

---

## Build 181 (v1.4.0 — June 20, 2026)

**For early access: a new Memory tab in History that shows what your coach has been remembering about each of your workouts — and lets you clear any of it.**

If you're in early access, History now has a third tab alongside Sessions and Progress: Memory. It lays out the notes your coach keeps on each of your workouts — what it's picked up about your Push, Pull, and Lower days — each tagged with how long ago it noticed, so you can see what's quietly shaping its advice. If a note is off or out of date, you can tell the coach to forget it and start that workout fresh.

---

## Build 180 (v1.4.0 — June 20, 2026)

**Tell your coach you're switching exercises and it actually switches — no more "finish this one first."**

When you jump to a different move mid-session — whether you tap it in your session map or just tell the coach "moving to overhead press" — your coach now follows you over to that exercise right away and sets you up with a weight and reps for it. Before, if you hadn't logged a set on your current move yet, the coach could dig in and insist you finish it first, sometimes a few times in a row. Now an explicit switch is taken as exactly that — you're moving on — so the coach comes along instead of holding you back.

---

## Build 179 (v1.4.0 — June 20, 2026)

**Weight chips that build around what you actually lifted, coach messages that survive an app reload, and — for early access — a new Progress view plus a refreshed session map.**

When you set the weight on a lift, the quick-pick chips now ladder around the weight you're actually using — edit a 200 lb set and you'll see 180 / 190 / 200 / 210 / 220 instead of the same fixed list every time — and the bodyweight option only shows up on moves where it fits, like weighted pull-ups and dips, not your barbell and machine lifts. We also fixed a slip where reloading the app just as your coach was mid-sentence — most likely right at the start of a session — could lose its message and leave a bare "Starting…"; the reply now saves as it streams in, so a reload brings it back. History also drops the old month-grid calendar and opens straight to your sessions list. If you're in early access, there's a new Sessions / Progress toggle in History — the Progress view charts how each exercise is trending, with badges that echo where your coach is steering you and chips to filter by plan — and the session map got a visual pass with equipment icons, the muscle worked under each move, and a slimmer card that shows your current lift front and center with a single rest countdown.

---

## Build 178 (v1.4.0 — June 19, 2026)

**The early-access session map now spells out each move — the gear and weight, the sets and reps you're after, and what you lifted last time.**

If you're in early access, the session map — your whole workout laid out move-by-move — now packs a lot more into each row. Every move shows the equipment and weight you'll use, with cardio and timed moves showing their length instead of a weight, plus the sets and reps you're aiming for, like "2 × 10". Moves you've done before also carry a quick "last time" line so you can see what you lifted on them, and the move you're currently on fills in a dot for each set as you knock them out.

---

## Build 177 (v1.4.0 — June 18, 2026)

**The early-access session map is easier to reach, sticks around as a slim card, and now carries your live time-left in one spot.**

If you're in early access, the session map we added last build — your whole workout laid out move-by-move — is easier to open now: instead of hunting for a small Map icon, just tap the time-left strip at the top of a planned session to pull it up. The map also stays put as a slim card through your session instead of disappearing when you close it — tap to expand the full timeline, tap again to shrink it back to a slim bar. And it now shows your time-left right on the card — minutes, sets to go, and a progress bar all in one place instead of two slightly different readouts side by side — and the minutes count down live while you rest.

---

## Build 176 (v1.4.0 — June 17, 2026)

**The live time-left strip is now on for everyone — and it finally counts cardio right, plus early access gets a tap-to-jump session map.**

The strip at the top of a planned session that shows roughly how many minutes and sets you've got left was early-access only until now — it's open to everyone in this build. We also fixed how it handles cardio and timed work: a planned 10-minute walk used to barely register toward the estimate, so cardio-heavy sessions read as much shorter than they really were — now timed moves count their full length and the time-left holds up. If you're in early access, there's also a new session map: tap the Map button in the session controls to see your whole workout laid out as a timeline — what's done, what you're on, and what's still ahead — and tap any upcoming move to jump straight to it.

---

## Build 175 (v1.3.5 — June 16, 2026)

**The time-left strip now counts down your rest, plus a logging fix when you jump to a new exercise.**

If you're in early access, the live time-left strip at the top of a planned session now folds in the rest you're currently taking — so while you're resting before your last set, it counts down the actual minutes you have left instead of reading "≈ 1 min" the whole time. For everyone, we fixed a logging slip where moving on to a fresh exercise you hadn't logged yet could file your set under the move you just finished — your set now lands on the exercise you're actually doing.

---

## Build 173 (v1.3.4 — June 16, 2026)

**Your coach gets to the point faster at the start of a session — and your first set lands on the right exercise.**

When you kick off a planned workout, the coach's opening message is leaner now: a quick hello, a one-line rundown of what's on deck today, and the weight to start with — no more walking you through how to log sets when you already know the ropes. Brand-new lifters still get the full welcome. We also fixed a logging slip where the very first set of a session could occasionally get filed under the wrong exercise from your plan — your opening set now sticks to the move you're actually doing.

---

## Build 172 (v1.3.4 — June 15, 2026)

**The coach now opens your session with your history already in hand — no more second-guessing the starting weight.**

When you kick off a planned workout, the coach used to go look up your past sessions on the spot, and once in a while it would think out loud about your first weight — landing on a number, then walking it back to another ("let's go 55… actually, 90"). Now it has your last session and the recommended next weight ready before it says a word, so its opening message lands on the right starting weight in one clean take. Nothing else changes about how it coaches you — it just gets there without the visible back-and-forth.

---

## Build 171 (v1.3.4 — June 15, 2026)

**The "why are you leaving?" sheet now waits for an actual answer.**

When you close the paywall and that quick "why?" sheet slides up, tapping the dimmed area behind it no longer dismisses it — a stray tap there used to count as a skip, which never really told us anything. Now the only ways out are picking a reason or tapping "Not now," so your answer reflects what you actually meant. If you're typing something in your own words, a new "Back" link lets you step back to the reason buttons.

---

## Build 170 (v1.3.4 — June 15, 2026)

**Two fixes that keep your session in sync when you switch exercises mid-workout.**

When the coach moves you on to a new exercise, the title at the top of your session now switches to that move right away instead of lagging behind on the one you just finished — so the header always matches the next-set chips below it. We also closed the last gaps in a recent fix: answering the coach's "what weight?" with just a number (like "40" or "50") no longer sneaks in a stray set, no matter how that number might've been read — it's always taken as the weight for your next set.

---

## Build 169 (v1.3.4 — June 14, 2026)

**Two logging fixes so the app keeps up when you switch exercises mid-session.**

When you tell the coach you're done with a move and ready for something else — like "bench is done, let's finish with a walk" — the tap-to-log rep chips from your last lift now clear out instead of lingering with stale numbers from an exercise you've already wrapped. We also squashed a glitch where repeating the same set a few times in a row could occasionally file your latest set under the next exercise on your plan instead of the one you're actually doing — your set now stays put on the current move.

---

## Build 168 (v1.3.4 — June 13, 2026)

**A clearer time-left strip for early access, plus a fix so answering "what weight?" never logs a phantom set.**

If you're in early access, the live time-and-sets strip at the top of a planned session is easier to read now — it's got a clock icon, the minutes stand out in the accent color, and a thicker progress bar. It also behaves better at the finish line: instead of quietly disappearing when you wrap your last set, it now says "All sets done," and it tucks away cleanly once the coach closes out the session. For everyone, we squashed a logging glitch where replying to the coach's "what weight?" with just a number could sneak in an extra one-rep set — that number is now correctly read as the weight for your next set, not a set you already did.

---

## Build 167 (v1.3.4 — June 13, 2026)

**See how much workout you've got left — early access gets a live time-and-sets estimate.**

If you're in early access, a planned session now shows a small strip at the top with roughly how many minutes and how many sets you've got to go, plus a progress bar that fills as you work through it. The estimate is smart about what's ahead — timed and cardio moves count their full prescribed time while lifts get a quick per-set estimate, with rest factored in — and it only shows up once you're mid-session on an actual plan. This build also brings a batch of reliability fixes for everyone: the coach's replies no longer garble when the connection hiccups, it reconnects cleanly instead of dropping a reply mid-answer, and it won't hang on a stalled stream. We also fixed the next-set chips occasionally disappearing, stopped a quick double-tap on Send or Finish from logging twice, kept set cards from bleeding across sessions, and cleaned up the Choose Workout grid so its second row no longer clips.

---

## Build 166 (v1.3.4 — June 12, 2026)

**Closing the paywall? Tell us why — one tap, totally optional.**

If you close the paywall without subscribing, a small sheet now slides up asking why — is it the price, do you want to train a bit first, or are you just looking around? One tap answers it, "Something else" opens a short text box if you'd rather say it in your own words, and "Not now" skips the whole thing. Jack says thanks and the sheet tucks itself away. It only appears once you've actually used the app a bit, and it won't pester you again right after you've answered.

---

## Build 165 (v1.3.4 — June 11, 2026)

**A safeguard so the paywall never advertises a free trial it can't deliver.**

The paywall now checks the live App Store offer before showing any "free trial" wording. In the rare case a trial offer isn't available, it falls back to plain "Subscribe · cancel anytime" copy instead of promising free days you wouldn't actually get. With today's standard 14-day trial in place nothing changes — you'll see the same trial copy as always.

---

## Build 164 (v1.3.4 — June 11, 2026)

**The free trial is now two weeks instead of one.**

New accounts now get a full 14-day free trial of Premium instead of 7, so there's more room to find your rhythm before deciding. The paywall reads the trial length straight from the live App Store offer, so the number you see is always exactly what you'll get — even right after we change it.

---

## Build 163 (v1.3.4 — June 11, 2026)

**Logged a set wrong? Tap its card and fix it on the spot.**

During an active session, every set card in the chat is now tappable — a small pencil in the corner marks the ones you can edit. Tapping opens the same big-numbers editor you know from History, so you can correct the reps or weight without breaking stride; the card updates with an "edited" stamp and the next-set chips recompute from the corrected numbers. The Choose Workout screen also got a visual pass: each plan tile now shows an expand glyph (instead of a magnifier) to open the full plan, the layout is cleaner with the body-part focus up top and the RECOMMENDED/LAST badge pinned to the bottom, and the selected plan gets a clear color tint.

---

## Build 162 (v1.3.3 — June 10, 2026)

**Preview a plan before you start it, and get tap-to-log chips on cardio too.**

The first time you're about to start a workout plan, it now opens up so you can look over the moves before diving in — and a magnifier on each plan in the Choose Workout list lets you peek at any plan on demand. Cardio and timed exercises now get the same tappable next-set chip a lift does, suggesting a duration from your last session even before the coach chimes in. We also fixed a couple of rough edges: tapping between sets in the Edit Session screen now shows the right reps and weight for the set you tapped (instead of leaving the previous set's numbers in the box), the Start button no longer goes briefly unresponsive while your data is syncing, and the coach now reads its full memory of your training instead of a version cut short mid-sentence.

---

## Build 161 (v1.3.3 — June 9, 2026)

**The fast tap-to-log set experience is now on for everyone.**

The tappable next-set chips above the chat box, the smart set card that shows how each set stacked up against last time, personal-record badges, and the cardio- and time-aware handling were all limited to early-access accounts — they're now open to everyone. Logging a set during a session is a one-tap affair for all users, and the coach reads from your full plan history when it sizes up your progress.

---

## Build 160 (v1.3.3 — June 9, 2026)

**A maintenance build — behind-the-scenes reliability work.**

No user-facing changes in this one. Some under-the-hood tidying to how the app handles sign-in and switching accounts (relevant mainly to internal testing). Everything you'd notice is already in place from earlier builds. On to the next.

---

## Build 159 (v1.3.3 — June 8, 2026)

**The coach won't log a set you didn't do.**

Saying something like "one more set of rows" or "back to squats" to steer the coach used to occasionally get logged as a completed set with made-up reps and weight. Now those steering phrases are treated as what they are — a request to keep going, not a set to record.

---

## Build 158 (v1.3.3 — June 8, 2026)

**Tap-to-log chips and a smarter set card make logging a workout set the fast way to talk to your coach.**

As you move through a session, the coach now offers tappable chips just above the chat box that suggest your next set — the reps to aim for, and for time-based moves a duration instead — so you can log a set with one tap rather than typing it out. Once you log it, a smart card shows how that set stacked up: how many more reps than last time, a badge when you've hit a personal record, and a nudge when you've pushed past your usual load. Cardio and bodyweight exercises are handled properly too — no more "x 0" on a reps-only move, and time-based exercises get their own card. The coach also got sharper: it asks for your weight when a lift needs one and it has nothing to go on, finds your past sets across your whole plan instead of just a recent window, and reports the actual reps you did (say 12, 10, 8) rather than flattening them to "3x10."

---

## Build 157 (v1.3.3 — June 6, 2026)

**No more little jump when a screen first appears.**

The bottom tabs (Train, History, Plans, Profile) and the sign-in and onboarding screens used to drop their content down by a hair the instant they loaded, as the app figured out where the notch and home bar were. That settling step is gone now — each screen lands in its final position on the first frame, so switching tabs and your first impression of sign-in feel cleaner and steadier.

---

## Build 156 (v1.3.2 — June 5, 2026)

**A maintenance build with under-the-hood housekeeping.**

No user-facing changes in this one — it's a version bump (1.3.1 → 1.3.2) with some behind-the-scenes tidying. Everything you'd notice from the last few builds is already in place. On to the next.

---

## Build 155 (v1.3.1 — June 5, 2026)

**A cleaner sign-in screen and a smoother way back in when your session ends.**

The sign-in and sign-up screens got a tidier layout: a single card with one clear primary button, an "or" divider, and Sign in with Apple in its natural spot — at the bottom on sign-in, up top on sign-up. Signing out or hitting an expired session now drops you on the Sign In screen instead of Sign Up, so getting back into your account is one less tap. We also fixed outbound links — the legal, store, and support links now fail gracefully with a clear message if your device blocks them (Screen Time or a work profile, say), rather than silently doing nothing.

---

## Build 154 (v1.3.1 — June 4, 2026)

**Editing past workouts is now open to everyone — fix a date, tweak a set, or log a session you forgot.**

The tools for cleaning up your history used to be limited to early-access accounts; they're now available to all. From the History list you can change a workout's date and time, edit or add sets, add an exercise, delete a session, and use the "Log a past workout" button to backfill anything you did away from the app. Coach Memory also got a visual pass for the early-access folks — the saved-to-memory and picking-up-where-we-left-off cards, the Coach Memory list, and the plan peeks all got a cleaner, more polished treatment, and progression notes now carry a concrete target like "135 → 140 next session." Behind the scenes we switched to sturdier crash reporting and folded bug reports and feature requests into a single feedback form in Settings, so getting word to us is simpler.

---

## Build 152 (v1.3.0 — June 2, 2026)

**The "Get set up" checklist stays done once you've done it, and the end-of-session Stop button can't be fired twice.**

Returning users were seeing "Get set up" pop back up with "Pick your coach" unchecked even though they'd already chosen a coach — the checklist was tied to device-wide flags that got wiped on every sign-in. It now reads from your real account state instead, so once you've picked a coach and customized a plan those items stay checked across logins. We also guarded the Stop button at the end of a workout: a quick double-tap used to fire the finish flow twice, so the first tap now dims and disables the button until the next session.

---

## Build 151 (v1.3.0 — June 2, 2026)

**A bigger, easier-to-read paywall and a close button that lines up right on every iPhone.**

The paywall had been shrunk down to fit the iPhone SE, which left it reading too small on the taller phones most people carry. It's now scaled up on those devices — a larger headline and subhead, an eyebrow that matches the rest of the app, and content that fills the screen instead of clumping at the bottom; the iPhone SE keeps its compact layout. The close ✕ on the onboarding screen also sits exactly where it should now, lined up with the header across the whole iPhone range from SE to the Dynamic Island models, instead of drifting into the status bar on some and below the title on others.

---

## Build 150 (v1.3.0 — June 1, 2026)

**Tap Start without a subscription and you'll land on the paywall first — plus a smoother sign-in screen.**

If you're not subscribed yet, tapping Start now takes you straight to the paywall instead of opening the workout picker, and once you subscribe it carries you right on to choose your workout; back out without subscribing and you're returned to the Train home. Paid users see no change. On the sign-in screen, the fields now scroll up out of the keyboard's way when you tap into them, so the box you're typing in stays visible — and tapping away still dismisses the keyboard. The close button on the onboarding screen also sits cleanly below the notch now instead of nudging the content down.

---

## Build 149 (v1.3.0 — June 1, 2026)

**Coach Memory you can actually see — plus a couple of moments where the coach shows its work.**

The coach's session memory now has a home: tap the new brain icon in History (alongside List and Calendar) to see the short note your coach kept after each workout, with the option to clear or forget any of them. You'll also catch it in the moment — when the coach saves a note at the end of a session a small "saved to memory" card appears in chat, and when you start a workout it's seen before, it opens with a "picking up where we left off" card quoting what it remembered. There's a Coach Memory shortcut in Profile and a one-line "Coach remembers…" peek on each plan, too. All of this is rolling out to early-access accounts first. Separately, tapping anywhere outside the fields on the sign-in screen now dismisses the keyboard.

---

## Build 148 (v1.3.0 — June 1, 2026)

**Drag to reorder your plans and exercises — and mark one-off workouts so they don't bump your rotation.**

The Plans tab is now a single list you can rearrange by dragging, with Rotation and Adhoc sections so it's clear which plans are part of your regular cycle. Open a plan and you can drag its exercises into whatever order you want, and flip an "Include in rotation" toggle to pull a plan out of the Last/Next cycle — handy for a one-off session that shouldn't push your push/pull/lower order forward. The coach now also remembers a short note from your last session and reads it back at the start of the next one, so it carries over tone and any cautions you mentioned without losing track of where your progression stands. That memory is rolling out to early-access accounts first.

---

## Build 145 (v1.2.3 — May 29, 2026)

**Backing out of the Apple sign-in sheet no longer throws a cryptic red error.**

If you tapped "Continue with Apple" and then changed your mind, dismissing the Apple ID sheet was surfacing a confusing error like "The operation couldn't be completed. (org.openid.appauth.general error -3.)". Cancelling is now treated as what it is — a quiet no-op — so the screen just returns to the sign-in form with nothing to dismiss. Genuine failures like a dropped network connection still show a real error, so nothing important gets swallowed.

---

## Build 144 (v1.2.3 — May 29, 2026)

**CrossFit moves, sleds, and weighted carries now live in the exercise library — and track properly.**

The library picks up a CrossFit tag spanning 38 exercises — olympic lifts, gymnastics, and conditioning staples, plus eleven new ones like wall balls, double unders, rope climbs, ring muscle-ups, the assault bike, and the ski erg. Carries and sleds (Farmers Carry, sled push/pull, yoke carry) get their own logging shape that tracks weight and duration side by side, so loaded carries finally record the way you actually do them instead of being forced into a reps box. Settings also got a little tidier: the duplicate Workout Plans row is gone (it's already a bottom tab), and long preference hints like the Rest Timer Bell note now wrap cleanly instead of shoving the toggle off the edge of the screen. Last, signing in with a fresh account no longer inherits the previous account's pre-checked "Get set up" steps — the checklist now resets on sign-in and sign-out so it reflects your account, not whoever used the phone before.

---

## Build 143 (v1.2.3 — May 28, 2026)

**Sign in with Apple on a device that's seen another account now drops you into a clean profile, not the previous user's name.**

Yesterday's Apple sign-in path cleared Cognito's token cache but left the app-level profile cache untouched — so a fresh Apple account would briefly inherit the prior email/password account's display name until the next profile sync caught up. The Apple sign-in flow now wipes both caches before saving the new tokens, matching what sign-out already did, so a new Apple account starts blank like it should. Also added a small note under the Rest Timer Bell toggle in Settings so it's clear the bell follows your iPhone's ringer switch — if your phone is on silent, the bell stays silent too.

---

## Build 141 (v1.2.3 — May 27, 2026)

**Sign in with Apple, and a cleaner sign-up flow to land on.**

You can now tap "Continue with Apple" on the sign-in and sign-up screens and get straight in — no password, no email confirmation step, just Face ID and you're through. The whole auth flow got a redesign at the same time: inputs are easier to tell apart from disabled buttons, the disabled state on the main CTA actually looks disabled, the coach pill no longer overlaps the headline on the Sign In and Reset Password screens, and password rules are checked before the button lights up so you don't bounce off a Cognito error.

---

## Build 140 (v1.2.3 — May 26, 2026)

**No more ghost typing dots floating in old chat threads.**

When the coach logged a set without saying anything out loud — silent tool-only turns — an empty bubble was getting saved to your chat history. The next time you reopened the app, it rendered as orphan typing dots that never resolved, scattered through the scrollback. The coach now skips saving those silent turns, and any ghosts already on disk are filtered out on load, so old threads clean themselves up the first time you open them.

---

## Build 139 (v1.2.2 — May 25, 2026)

**Biff is now Jack.**

The male coach goes by Jack from now on — same voice, same style, just a name that fits him better. The change runs everywhere the old name appeared: chat, coach picker, profile, welcome flow, and any prompts the coach uses to refer to himself. If you'd picked Biff before, you'll see Jack on next launch with no action needed. Kelly is unchanged.

---

## Build 138 (v1.2.2 — May 23, 2026)

**When the coach calls it a wrap, a red Stop button slides in next to Send so you can end the session with one tap.**

At the end of a planned workout the coach now signals that you're done — and the chat input grows a Stop button on the left, right where your thumb already is. Tap it and the session finishes through the same path as the Finish button up top, so you still get the post-workout recap. The button sticks around if you background the app mid-wrap, and disappears the moment the session ends.

---

## Build 137 (v1.2.2 — May 23, 2026)

**Maintenance build.**

No user-visible changes this round — a version bump to 1.2.2 on top of build 136 with the same feature set.

---

## Build 136 (v1.2.1 — May 23, 2026)

**After a PR, a clean weight push, or a workout-count milestone, the coach now asks if you're loving it — and if you say yes, you're handed straight to Apple's write-a-review screen.**

When a session ends on a real high, Biff or Kelly drops a one-liner in chat and a small "Love it / Not really / Dismiss" sheet slides up. Tap Love it and you go to Apple's combined stars-and-text review screen — the App Store's own UI, not a mimic. Tap Not really and you get an in-app feedback form, so the rough edges land in front of us instead of as a one-star public review. Each path has its own cool-off — 90 days after a positive, 60 after feedback, a week after a dismiss — and your first couple of workouts plus any deload session are kept quiet, so the ask only ever shows up on a genuinely good moment.

The first cut accidentally treated any finished cardio block as a "weight push" — a bodyweight or duration-based history has no weight axis to progress on, so the suggestion came back as `suggestedWeight: 0` and the gate triggered on essentially every walk. That's fixed: reps-axis exercises are skipped entirely, since rep progress is already captured by the PR trigger.

Two reliability fixes ride along. The History tab now loads its sections — active session, completed sessions, and current plan — independently, so a hiccup in one no longer blocks the others from showing. And if the coach ever gets stuck in a tool-calling loop, it bails after a few rounds with a "Coach got stuck — try again" message instead of churning silently against the daily token cap.

---

## Build 135 (v1.2.1 — May 22, 2026)

**Correcting a set in chat now updates that session in your History tab, not just the chat card.**

Build 132 fixed the chat scrollback so a corrected set re-renders in place. The History tab had the same blind spot one level up: a session card only redrew when the number of sets or exercises changed, so a correction that swapped an exercise or changed reps, weight, notes, or equipment left the counts identical and the card kept showing the pre-correction values. The card now redraws whenever any value on it actually changes, so your chat and your history finally agree everywhere.

Also tightened up account handling: signing out now fully clears the previous account's in-memory workout plan and exercise data, and a program sync that fires mid-switch is blocked from writing to the wrong account. This only ever surfaced when switching accounts on one device, but it's the kind of bug that quietly corrupts data, so it's now closed off on both sides.

---

## Build 134 (v1.2.1 — May 21, 2026)

**Finish a set of bodyweight pull-ups or push-ups and the coach now gives you a rep target for next time instead of going quiet.**

The coach's progression call only knew how to talk about weight. On a bodyweight exercise — pull-ups, push-ups, dips with no added load — it had no weight to suggest, so it just skipped the call and moved on to the next move with nothing. Knock out 5/5/4 bodyweight pull-ups now and the coach reads the same flat/descending/dropping patterns it always has, then states the next-session target on the reps axis: push for 6 next time, hold at 5, or back off — whichever the numbers say. No more silent advance, and no more nonsense "go up 5 lb" on a movement that doesn't have a weight.

---

## Build 133 (v1.2.1 — May 21, 2026)

**Telling the coach a set belonged to a different exercise now cleans up the wrong card and logs the right one in the same breath.**

If you said "that last Bicep Curl was actually a Seated Row," the coach used to log the Seated Row but leave the bogus Bicep Curl card sitting in chat and in History. Now it deletes the misfiled set and logs the correction in one turn, and the chat thread drops the old card in place so the scrollback stays honest. Your session ends up with what you actually did, not what the coach misheard.

---

## Build 132 (v1.2.1 — May 21, 2026)

**Correcting a logged set in chat now updates the set card right there in the scrollback.**

If you told the coach "that was bodyweight, not -30 lbs" and it corrected the set, the History tab picked up the new numbers but the card in the chat thread kept showing the old ones — reps, weight, equipment, all stale. The card now re-renders the moment the correction lands, so the conversation and your history agree.

---

## Build 131 (v1.2.1 — May 21, 2026)

**Cardio rows from your plan now always pick up the CARDIO eyebrow, even on the first set of a fresh session.**

There was a race where logging the first set of a planned cardio exercise — "Walking," say — could land without the CARDIO eyebrow or body-part chip on the set card if the exercise library hadn't finished loading yet. The name was right, the duration and distance were right, but the row looked like a plain lift. The coach now pulls that metadata straight from your plan when the library isn't ready, so the eyebrow shows up reliably from the first set on.

---

## Build 130 (v1.2.1 — May 21, 2026)

**A big-numbers editor for sets and session timing — large value, small unit, a ± stepper, preset chips, and a number pad that stays put.**

Tapping a set in History now opens a redesigned editor: the value you're changing is huge and front-and-center, with a small unit beside it, a ± stepper for one-at-a-time nudges, preset chips for common jumps, and a number pad that stays put instead of fighting you for screen space. Same shell handles every kind of set — strength with reps and weight, bodyweight with just reps, assisted moves (which now correctly show the assist as a leading minus), and cardio with duration and distance. Editing when the session happened and how long it ran uses the same panel, so it all feels like one thing.

---

## Build 129 (v1.2.1 — May 2026)

**The chat input is back to behaving, and cardio rows speak their own language again.**

If your plan has "Walking" in it, the coach now logs your walk as "Walking" instead of "Walk" — so the cardio eyebrow shows up on the set card and the entry lines up with the plan. Off-plan stuff still logs freely under whatever name fits ("Burpees" doesn't get forced into the nearest plan match). Cardio set cards also now render distance with its unit — "0.5 mi" instead of a bare "0.5" — so the row stops looking like a half-set of something countable.

On the chat input: the send/play button is nudged up a few pixels so it sits at the text baseline instead of low, and the character counter is hidden until you cross 4000 characters. Below that it was just noise; from 4000 on you actually want the budget signal, with the orange warning still kicking in at 4750. When it does appear, it lives inside the bar above the button instead of floating in the gap above the input.

---

## Build 128 (v1.2.1 — May 2026)

**The set editor stops covering the row you're editing, deleting a set is one tap with an undo, and the coach stops fibbing about what's logged.**

The History edit modal got another round. Tapping a set now slides up a panel from the bottom of the sheet while the list above it shrinks, so the row you're editing stays in view instead of being covered by a centered dialog. The row itself highlights so the panel's context is obvious, and the same panel handles editing when the session happened — opening one closes the other. The "· Set N" suffix in the panel title is gone, the row densities are tighter, and the first field actually focuses after the slide settles instead of racing it.

Deleting a set no longer pops a confirmation modal — tap the delete, the set goes, and an "Undo" toast hangs around for six seconds in case you didn't mean it. The toast button is bigger than it looks (extra hit slop) and labeled properly for VoiceOver.

On the coach side: if you ask "did it log?" or "log the walk?", the coach now checks the current session before answering instead of cheerfully claiming "Already logged, you're good" when it isn't. And if you fire off a self-contained report — "just walked 0.6 miles in 11 minutes" — that gets logged as a walk even when the active exercise is something else (lifts, mid-warmup, whatever). Previously those could fall through the cracks if the coach had just transitioned to a different movement.

One more History fix: legacy exercises logged before the category-snapshot work shipped now classify against the library, so duration-only moves like "Sauna Stretch" stop sprouting a phantom miles field, and older walks/runs keep both their duration and distance.

---

## Build 127 (v1.2.1 — May 2026)

**Saving a set edit now scrolls the row back into view.**

When you save an edit in the History modal — especially "+ Add set," which lands the new row at the bottom of its exercise card — the row could end up below the fold if the sheet had been scrolled up. The list now scrolls to the saved row as the dialog closes, with a bit of breathing room above so it doesn't sit flush against the summary bar. Small thing, but you get to actually see the save land.

---

## Build 126 (v1.2.1 — May 2026)

**The set-edit dialog stops crowding the keyboard, and the coach stops occasionally double-logging your sets.**

The dialog that opens when you tap a set was centering itself vertically, which left Save/Cancel pressed up against the top edge of the keyboard — fine for a weighted set with one input, cramped for a cardio set with two. It now anchors near the top of the sheet with a clear gap above the keyboard, and the first field focuses on open so you can start typing immediately.

Under the hood, the coach had a path where it could log a batch of sets without going through the scribe — which meant a set you'd already logged could quietly get re-logged a second time. That route is now properly closed.

---

## Build 125 (v1.2.1 — May 2026)

**Editing a set opens a proper sheet, and the sign-in screen finally plays nice with password managers.**

The History edit modal's per-set editor used to swap the row into edit mode in place, which kept fighting the keyboard for space — the focused row could scroll out of view, and the fixes for that kept reintroducing the old double-inset problem. Tapping a set now opens a small dialog over the dim layer with the reps/weight fields and Save/Cancel buttons, sitting cleanly above the keyboard every time. The row stays in read mode and is fully tappable; "+ Add set" still appends an empty set and opens the same dialog.

On the auth screen, the email and password fields now advertise themselves properly to 1Password, iCloud Keychain, and the rest, so autofill suggestions actually show up. "Forgot Password?" moved out from under the email field to under the Sign In button where you'd expect it. The chat input font is also back to 16pt after a stray tweak nudged it down a couple of points earlier in this cycle.

---

## Build 124 (v1.2.1 — May 2026)

**The edit modal does its job inline, and the coach stops being coy about weight bumps.**

The History edit modal got another round of polish. Typing into a reps or weight field now replaces what's there instead of appending — type "20" on a "15" and you get 20, not 1520. The add-exercise picker grows a "From your plans" section at the top, so a movement you already programmed is one tap away instead of buried in Library. The edit-timing dialog goes back to tap-outside-cancels (so a stray tap mid-spin doesn't commit a wrong date), and the date picker is finally legible on the dark sheet. The sheet itself stops overshooting when the keyboard comes up on short modals.

Since the editor can now fix anything you'd want to fix, the "Tell coach about this" affordances are gone — no more tip bar, per-exercise pill, or action-sheet item routing you back into chat to describe a logging mistake you could just correct in place.

On the coach side: after a session where you hit your reps flat, it now actually states the new weight it's bumping you to instead of saying "nice work, 3x10 — moving to next" and leaving you to guess. And if your set reps weren't flat — say 10/9/9 — it reports them verbatim instead of rounding to "3x10".

---

## Build 123 (v1.2.1 — May 2026)

**Editing a single-set workout no longer hides the row behind the keyboard.**

When the edit-session sheet only had one set in it, tapping the reps or weight field used to scroll the row clean off the top of the screen — two different keyboard-avoidance mechanisms were both lifting the content, so the row overshot into nowhere. The sheet still rises above the keyboard, but the inner list no longer double-pushes, so the focused row stays put whether you're editing one set or twenty.

---

## Build 122 (v1.2.1 — May 2026)

**No more double-ding, and bodyweight moves stop pretending they need weight.**

Two paths could chime the rest-timer bell at the same time. If you were watching the screen when rest ended, the lock-screen banner was carrying audio on top of the in-app chime — that banner now shows silently in the foreground so only the in-app sound plays. And if you briefly tapped back into the app within a few seconds of a backgrounded ding, the in-app timer used to fire a follow-up chime; it now knows that notifee already handled the audio and stays quiet.

Push-ups, ab wheel, bird dog, and other bodyweight moves no longer render a weight column in the editor or read view — they're reps-only now, which is what they always should have been. Cardio-only sessions stop showing a misleading "1 reps" or "0 reps" on the session card, since legacy walks were quietly logged with a single rep. The reps stat just disappears when there's nothing meaningful to count.

---

## Build 121 (v1.2.1 — May 2026)

**Log a workout you forgot, fix when it happened, and a bigger chat input.**

The History tab gets a "+" button for logging a past workout — pick the type, the edit modal opens pre-filled with today's date and 60 minutes, and you fill in the rest. Tapping the date on any session now lets you change when it actually started and how long it ran. Cardio rows show their unit ("2 miles", "0.5 miles") instead of a bare number, and older walks, runs, and bikes that were locked to duration-only can finally have distance edited too.

The edit modal itself got a round of polish: tap outside the sheet to dismiss when you haven't changed anything, "+ Add set" starts blank instead of pre-filling your last set's reps and weight, and single-digit reps line up with double-digit ones so the column stops jittering between rows. A sync bug is also gone — edits and deletes made from History no longer get clobbered when the in-progress session finishes.

In the Train tab, the chat input now holds up to three lines before scrolling inside itself, so longer messages don't get their descenders clipped at the bottom of the pill.

---

## Build 120 (v1.2.1 — May 2026)

**No double-ding when you come back to a finished rest.**

If you backgrounded the app mid-rest, the lock-screen notification already fired when the timer hit zero — but reopening the app would chime a second time as the in-app timer caught up. The in-app chime now only fires for rests that ended within the last few seconds, so a stale timer stays quiet. The haptic still pulses when you return, so you get the tactile cue without the redundant audio.

---

## Build 119 (v1.2.1 — May 2026)

**The rest-timer bell rings through a locked phone, and it stops pausing your music.**

The bell now fires as a local notification when the app isn't in front, so you'll hear it whether the phone is locked, in your pocket, or you've swiped over to Spotify. While the app is foregrounded, audio playback now mixes with whatever else is playing instead of taking over the audio session — your music keeps going, the chime layers on top.

If you're in early access, past sessions are now editable from History: tap a set to inline-edit, "+ Add set" to append one prefilled from your last, or "+ Add exercise" to attach a movement you forgot to log. A nagging sync bug is also fixed — deleting a custom exercise or plan entry no longer resurrects it on the next launch. Small polish: the keyboard now dismisses when you drag the chat list or the exercise picker, and the plans editor lets you save a plan with as few as one exercise.

---

## Build 118 (v1.2.0 — May 2026)

**The rest-timer bell rings on time, every time.**

The boxing-bell sound is now loaded into memory the moment the app starts, so the first ding of a session fires the instant your rest ends instead of after a brief lag while the file decoded. Subsequent rings were already snappy — this brings the first one in line.

---

## Build 117 (v1.2.0 — May 2026)

**Maintenance build.**

No user-visible changes this round — a republish on top of build 116 with the same feature set.

---

## Build 116 (v1.2.0 — May 2026)

**A boxing bell when your rest ends, and set cards that show what they are.**

If you're in early access, there's a new Rest Timer Bell toggle in Settings — flip it on and the rest period ends with a quick boxing-bell ding so you don't have to keep glancing at the phone. Toggling it on plays a preview right then, which doubles as a check that your device isn't on silent.

Logged set cards now carry a small metadata strip — a colored category eyebrow (DUMBBELL, REPS ONLY, DURATION, etc.) plus body-part dot chips — matching the look of the plans editor, so a glance at the card tells you what kind of movement it was.

The coach stops asking how long you want to do cardio up front; it now proposes a specific duration based on what you've done in recent sessions instead of making you commit before the warmup. The silent scribe got a bulk-log tool so a quick "did 5x5 at 185, then 3x10 at 135" files in one shot instead of one call per set, and references to internal tools and agents no longer slip into the coach's replies.

---

## Build 115 (v1.2.0 — May 2026)

**The coach notices what you skipped, and the scribe stops double-logging follow-up sets.**

If your plan had four exercises and you only got through two before wrapping, the coach now flags the un-started ones at session close instead of letting them slip by quietly. The silent scribe got another duplicate-log fix — it was occasionally re-logging follow-up sets in the same exercise; now it sees full session state and only files each set once. Small UI polish: the coach avatar is the same size across Train, History, Plans, and Settings.

---

## Build 114 (v1.2.0 — May 2026)

**Plans is out of early access — everyone gets it.**

Workout plans are now available to all users, not just the early-access group. The Plans tab is on by default and the old "Enable Plans (Preview)" toggle has been removed from Settings since there's nothing left to toggle. The version bump to 1.2.0 marks the milestone — Plans has graduated from preview to a first-class part of the app.

Under the hood, the silent scribe got another sharpening: a prod failure where it would tag a bare rep against the wrong exercise mid-multi-set is fixed by a tighter prompt that keeps it locked onto the active exercise.

---

## Build 113 (v1.1.6 — May 2026)

**Maintenance build.**

No user-visible changes this round — just behind-the-scenes work on the scribe's test harness and prod transcript capture so we can keep tuning it from real sessions.

---

## Build 112 (v1.1.6 — May 2026)

**Corrections actually stick, and the silent scribe is now on for everyone.**

If you fixed a set after logging it ("actually that was 185, not 175"), the History tab updated but the set card in chat kept showing the old number — so the chat looked like it had ignored you. The card now updates in place when you correct or delete a set, with a small edited indicator so you can see the change took. Deleting a set also renumbers the cards after it so the indices match what History shows.

The background scribe — the silent logging agent introduced a few builds back — is now running for everyone, not just early access. Alongside that, it got noticeably sharper: it stops misreading a correction as a brand-new set, ignores meta-talk like "remind me when I'm done" or "stop logging" instead of trying to file it as a workout, and does a better job telling who said what in a fast-moving exchange.

---

## Build 111 (v1.1.6 — May 2026)

**Train got a visual tune-up.**

The chat surface now follows the latest design system: user and coach bubbles share the same shape and padding, with a thin colored stripe down the left side carrying each side's identity color instead of filling the whole bubble. Set cards got the same treatment — one consistent style with a green left rail and a simple ✓, whether you're in a real session or the welcome demo.

The input bar is clearer about state too: a play button when you're ready to start, a dimmed send icon when the input is empty, and a bright send arrow once you start typing. The Start Session button picks up your coach's accent color (orange for Biff, yellow for Kelly), and the bottom tab bar now tints to match your coach as well.

---

## Build 110 (v1.1.6 — May 2026)

**The scribe stops double-logging your sets.**

If you rattled off a few sets in quick succession, the background logging agent would sometimes re-log sets it had already saved — it was seeing old messages and didn't know what was already recorded. That's fixed: the scribe now only looks at the most recent exchange and knows exactly which sets exist, so each rep report is logged once and only once.

---

## Build 109 (v1.1.6 — May 2026)

**You can export your data, and the coach actually knows the plan.**

There's a new "Export History" option in Settings that dumps your entire workout history to a CSV file — exercises, sets, weights, units, and all. Share it, graph it, back it up, whatever you want.

The coach now opens each session with a quick preview of what's on deck ("4 sets of bench, 3 sets of rows…") and tracks your progress against those targets as you go, so it knows when you've hit your planned volume and when there's more to do. The preview is concise — just exercises and set counts, no weight chatter.

A handful of miscategorized exercises in the library have been corrected, and the first-time experience got a pass to make Train, History, Plans, and Profile each feel useful from the jump instead of mostly empty.

---

## Build 107 (v1.1.5 — May 2026)

**Plans is easier to find, and the session subtitle stops lying.**

If you're in the early-access group, Plans is now surfaced where you'd actually look for it: a hint on the first-time welcome card, and a clearer cog on the "Choose Workout" modal so you can jump straight into the editor. The default Push/Pull/Lower template now has a small info icon next to Reset to Default that explains the thinking behind it — compound lifts, recovery between workouts, progressive overload — for anyone curious about the shape of their starter plan.

Bug fix: when you started a session on a custom workout type (say, "Ben"), the subtitle on the session card sometimes read "Lower day" or whatever the next-up suggestion was, even though the coach was correctly working on Ben. It now reads the workout you're actually in.

---

## Build 106 (v1.1.5 — May 2026)

**The coach stops logging sets — a silent scribe takes over.**

Logging now runs in parallel as its own background agent, so the coach can focus on talking instead of juggling tool calls. The set chip appears right after the coach's reply, and you won't see double-logs or stray recaps of what was just logged.

Cardio is cleaner too: the coach won't invent a distance or duration when you only give it one, and a correction now merges into the existing set instead of overwriting it (so fixing the weight doesn't wipe the duration).

Plans got a rename action via a bottom sheet, with a heads-up if the change would affect your history. Sync is sturdier — your program won't get clobbered on login, pending uploads retry with backoff, and anything queued while offline replays on reconnect. Smaller polish: empty plans are skipped when recommending the next workout, the coach won't keep nagging you to tap Finish after you already did, and new users get a refreshed Push/Pull/Lower seed.

---

## Build 104 (v1.1.4 — May 2026)

**Maintenance build.**

No user-visible changes in the app this round — just minor under-the-hood cleanup.

---

## Build 103 (v1.1.4 — May 2026)

**Coach only logs a set when you report one.**

Follow-up to last build's bootstrap fix: the trigger to log a set is now strictly *your* last message, not anything the coach itself said. So if the coach recaps "nice, that's three sets of squats" or otherwise narrates back to you, it won't double-log — only your own reports count.

---

## Build 102 (v1.1.3 — May 2026)

**Workout Plans, properly: build a program from a real exercise library.**

Plans now has its own tab, with a structured editor instead of a chat builder — pick exercises from a Strong-based library of hundreds of moves, filter by body part or category, and build out your week directly. Search is smarter too: typing "tricep p" finds "Triceps Pushdown", and results are ranked by relevance instead of alphabetical. You can add and edit your own custom exercises, and they sync across devices automatically. While a session is live the plan editor goes view-only so a mid-workout edit can't confuse the coach — finish the session, then edit.

The coach got a few fixes: it can now delete a set if it logs the wrong one, it knows which category each plan exercise is (so it coaches a Lat Pulldown like a pulldown, not a generic lift), and it won't auto-log a "walk" on the very first message of a session anymore.

---

## Build 101 (v1.1.2 — May 2026)

**Workout Plans preview is back to early access only.**

The "Workout Plans (preview)" toggle in Profile → About You is gated to early-access testers again while we keep iterating on it. If you don't have early access, the toggle won't appear — your existing workouts and coaching are unaffected.

---

## Build 100 (v1.1.2 — May 2026)

**The coach logs everything and stops mistaking warmups for working sets.**

If you report an exercise that isn't on today's plan, the coach now just logs it and moves on instead of pushing back — extra work and substitutions count. Warmup sets are also kept separate from working sets when the coach decides whether to bump weight, hold, or drop, so a few light primer sets at the top of a session won't get read as a collapse and trigger a false drop. Recaps split warmups out from working sets too, so the volume you actually did is easier to see.

---

## Build 99 (v1.1.2 — May 2026)

**Workout Plans preview is open to everyone.**

The "Workout Plans (preview)" toggle in Profile → About You is no longer gated to early-access testers — anyone signed in can flip it on and start building custom training programs. The feature itself is still opt-in, so nothing changes if you don't turn it on.

---

## Build 98 (v1.1.2 — May 2026)

**History in your colors, and the coach knows your plan.**

If you've set up custom workout types, History now uses your colors for both the chips on each card and a tinted card background that matches — much easier to scan at a glance. The coach also reads your active workout plan from the first message of a session, so it knows your program without you having to spell it out. Plan editing is now locked while a session is live, so a mid-workout edit can't confuse the coach — finish the session, then edit.

---

## Build 97 (v1.1.2 — May 2026)

**Maintenance build.**

No user-visible changes in the app this round — just minor under-the-hood cleanup.

---

## Build 96 (v1.1.2 — May 2026)

**Maintenance build.**

No user-visible changes in the app this round — just minor under-the-hood cleanup.

---

## Build 95 (v1.1.2 — May 2026)

**Tap a Jacked link, land in the app.**

Links to `jackedapp.ai/open` now open the Jacked app directly if you have it installed, instead of bouncing through Safari. If the app isn't installed (or you're on Android or desktop), the same link falls back to a friendly page with an App Store button. The rest of this build is behind-the-scenes infrastructure — staging environment cleanup and email-template fixes — none of it user-visible.

---

## Build 94 (v1.1.2 — May 2026)

**Shorthand-logging fix.**

Typing shorthand like "2x10x70" mid-session was only logging one set instead of two — the coach now correctly logs every set when you use that format.

---

## Build 91 (v1.1.0 — May 2026)

**Redesigned History edit, smarter progression, and a cleaner About You.**

Editing a past session now opens a full-height sheet that matches the redesign — a workout summary up top, cleaner exercise and set rows, an overflow menu in the header (where Delete Workout now lives), and an Undo toast if you remove a set by mistake. On an active session, each exercise has a "Tell Coach" shortcut that hops over to chat with the exercise pre-mentioned. Progression coaching no longer assumes you train in a fixed rep range — it now reads your own history to decide bump, hold, or drop, so a flat 6/6/6 or 12/12/12 both register as "weight's too easy" without any setup. The About You sheet was rebuilt: weight and height share a row, height shows ft/in inline, and age is now stored as birth month + year (we don't ask for the day) so it stays accurate as you get older.

Also fixed: plan names like "Pull" now render the correct color in History instead of grey, the onboarding X button no longer clips the status bar, and returning users aren't blocked on the "How did you hear about us?" screen.

---

## Build 90 (v1.1.0 — April 2026)

**Smarter rotation with custom plans, and onboarding polish.**

If you've turned on custom workout programs, the coach now recommends your next session in the order you set — instead of falling back to the default push/pull/lower rotation. Modal sheets are fully opaque again (the translucent look was letting the wrong things bleed through), while chat cards stay translucent as designed. Onboarding's "How did you hear about us?" picker also got proper social icons, an App Store option, and tighter card spacing.

---

## Build 89 (v1.1.0 — April 2026)

**Sessions survive app reloads, plus a new onboarding question.**

If iOS reloaded the app mid-workout, your conversation with the coach used to reset — now the full chat history comes back exactly where you left it, alongside the set cards and plan exercises that already persisted. Plan exercises now restore for everyone on reload, not just users on the preview flag. Onboarding also adds a quick "How did you hear about us?" picker so we can learn what's working.

---

## Build 88 (v1.1.0 — April 2026)

**Shorthand logging and smarter offline catch-up.**

Type "4x8x225" and the coach now logs four sets of 8 at 225 without asking what you meant — standard shorthand just works. If you trained offline or logged somewhere else, you can now dump your whole workout at once and the coach logs everything immediately, then gives you a quick summary instead of checking in set by set. Also fixed: set cards were disappearing when iOS backgrounded and restarted the app mid-session — they now survive the restore correctly.

---

## Build 87 (v1.1.0 — April 2026)

**Smarter progression coaching and Workout Plans polish.**

The coach now tracks your progression data and calls out weight increases at exactly the right moment — when you've nailed the rep target, it tells you to add weight next set. It's also less verbose about it: one sentence, no lectures. Your workout plan exercises are seeded into the session from the start, so the coach knows your program before you say a word. History now labels each session with the plan name, and the plan editor was upgraded to use the same input bar as the main chat.

Also fixed: autocorrect swapping text after you tapped Send, and a workout picker label that was getting clipped.

---

## Build 86 (v1.0.4 — April 2026)

**Onboarding layout fix for smaller phones.**

The onboarding screens were overflowing on compact devices like the iPhone SE and iPhone 14. Fixed — everything fits cleanly regardless of screen size.

---

## Build 85 (v1.0.4 — April 2026)

**Build your own workout programs.**

Workout Plans is now available as a preview — enable it in Profile → About You to get started. You can create and manage custom training programs, and each plan has its own coach you can chat with to add, swap, or remove exercises. Your session coach also now knows about your plans, so it can reference them while you're mid-workout. A handful of plan-editor fixes landed too: the exercise list stays visible while you edit, auto-scroll no longer fights you during streaming replies, and the coach handles edge cases (like removing an exercise that's already gone) gracefully.

---

## Build 84 (v1.0.4 — April 2026)

**Onboarding refinements.**

The new onboarding screens got a second pass to lock in the details — a close button in the top-right so you can skip at any point, a back link under each CTA so it's easy to step back, and type and button copy tightened up to match the final design.

---

## Build 83 (v1.0.4 — April 2026)

**New onboarding and a livelier splash screen.**

The onboarding flow has been fully redesigned — four screens that show the real app UI so you know exactly what you're getting before you start. The splash screen now has a sparkle pop animation as the wordmark and tagline come in. Copy and type details throughout onboarding have also been tightened up to match the final design.

---

## Build 82 (v1.0.4 — April 2026)

**Chat input bar touchup.**

The send button, play button, and input pill at the bottom of the chat screen now match the design exactly — correct sizes, colors, and borders. Nothing functionally changed, just looks crisper.

---

## Build 81 (v1.0.4 — April 2026)

**Visual polish across Train, History, and Profile.**

The Train, History, and Profile tabs have been pixel-matched to the latest design — tighter spacing, better alignment, and cleaner type across all three screens. Also fixed a cosmetic glitch where a blank message bubble would briefly appear in the chat after you sent a message.

---

## Build 79 (v1.0.4 — April 2026)

**Rest timer now taps your shoulder.**

When a set is logged, Jacked schedules a local notification so you know when rest is up — even if the app is in the background. You'll be asked for notification permission once after onboarding. Onboarding itself has been fixed so it only shows on your very first launch, not every time you open the app.

---

## Build 77 (v1.0.4 — April 2026)

**Stability update.**

No new features in this build — same as build 76. Version bump for App Store submission.

---

## Build 76 (v1.0.3 — April 2026)

**History filters, sharper icons, and a cleaner splash.**

The History tab now has filter chips so you can quickly narrow to Push, Pull, or Lower sessions. The workout picker shows which type you last did and flags any session that's still in progress. Icons across the app are now crisp vector graphics instead of PNGs — noticeably cleaner on all screen sizes. The splash screen wordmark got a few polish fixes too.

---

## Build 74 (v1.0.3 — April 2026)

**Milestones, a faster coach, and smarter routine prompts.**

Your all-time personal records are now front and center in milestones, with a new goal sequence and a View All sheet to scroll through everything you've hit. The coach is noticeably faster to respond. The routine prompt now shows up at the right time — when you first try a new workout type, not during setup.

---

## Build 73 (v1.0.3 — April 2026)

**Milestones, a faster coach, and smarter routine prompts.**

All-time personal records are now highlighted in milestones, with a refreshed goal sequence and a View All sheet to browse your history. The coach responds faster. The routine prompt now surfaces at the right moment — the first time you try a new workout type, not during initial setup.

---

## Build 72 (v1.0.3 — April 2026)

**Milestones, a faster coach, and smarter routine prompts.**

All-time personal records are now front and center in milestones, with a fresh goal sequence and a View All sheet to browse everything you've hit. Coach replies are noticeably faster. The routine prompt now appears at exactly the right moment — the first time you try a new workout type, not during initial setup.

---

## Build 71 (v1.0.3 — April 2026)

**Milestones, a faster coach, and smarter routine prompts.**

The milestones section now shows all-time personal records with a fresh goal sequence and a View All sheet to browse everything you've hit. Coach replies are noticeably faster. The routine prompt appears at the right moment — the first time you try a new workout type, not during initial setup.

---

## Build 69 (v1.0.2 — April 2026)

**Smarter routine prompts.**

The first time you try a new workout type, the coach now asks if you already have a routine for that specific session — so if you've got a Push Day program, it offers to use it right when it's relevant. The generic routine tip that appeared during initial setup has been removed.

---

## Build 67 (v1.0.2 — April 2026)

**Milestones and a faster coach.**

The milestones section has been reworked — it now shows all-time personal records, a fresh goal sequence, and a View All sheet so you can browse everything you've hit. Coach replies are noticeably faster.

---

## Build 66 (v1.0.2 — April 2026)

**Spacing polish.**

A bit more breathing room between the chat input and the keyboard on all devices. History workout cards also have slightly better spacing so they're easier to scan.

---

## Build 65 (v1.0.2 — April 2026)

**Edit and delete from history.**

You can now tap into any logged workout and edit or delete individual sets, or remove the whole session if needed. Coach chat got a visual refresh — fonts are sharper and the coach's message bubbles now use a color that matches their coaching style. Login sessions are stored in the iOS Keychain so you stay signed in more reliably across app updates.

---

## Build 63 (v1.0.2 — April 2026)

**Chat input polish.**

The input bar now collapses and clears automatically when a session ends, so it's out of the way until you need it again. You can also type your next message while the coach is still responding — no more waiting. A bit more breathing room was added between the input bar and the keyboard.

---

## Build 62 (v1.0.2 — April 2026)

**Keyboard fix.**

Fixed a gap between the chat input bar and the keyboard on real devices — the input now sits flush against the keyboard as intended.

---

## Build 61 (v1.0.2 — April 2026)

**Password reset, security hardening, and Rate the App.**

Reset password flow now has correct labels and no longer shows confusing Cognito error messages. Sign-in no longer reveals whether an email is registered. Rate the App in Settings is now wired up. Dev settings panel is accessible by tapping the staging banner.

---

## Build 59 (v1.0.2 — April 2026)

**Account switching and input polish.**

Toggling between staging and production now fully swaps your account — profile, history, and conversation all switch. Chat input is capped at three lines so it doesn't take over the screen.

---

## Build 58 (v1.0.2 — April 2026)

**A play button.**

A play button in the chat input lets you start a new workout session without reaching for the header. New users are reminded they can paste an existing routine to get started.

---

## Build 57 (v1.0.2 — April 2026)

**Staging indicator and floating tab bar.**

A banner appears when the staging API is active so it's always clear which environment you're on. The tab bar now floats above the content. Also fixed a bug where warmup sets were sometimes auto-logged before you confirmed them.

---

## Build 56 (v1.0.2 — April 2026)

**Welcome email and website performance.**

New users now receive a welcome email after signing up. The website was overhauled — fonts, images, and layout are all faster and sharper. No app behavior changes.

---

## Build 51 (v1.0.2 — April 2026)

**Removed beta mode.**

The beta escape hatch for access control has been retired. Access is now fully controlled by your subscription. No visible changes if you're a subscriber.

---

## Build 50 (v1.0.2 — April 2026)

**Coach identity is live for everyone.**

The redesigned coach chat experience — new bubble styles, session header, and refined typography — is now on for all users. Also removed the How It Works rotator from the sign-up flow to keep onboarding focused.

---

## Build 46 (v1.0.1 — April 2026)

**Header and dev panel polish.**

History and Profile tab headers cleaned up. Staff dev panel refined. No behavior changes for regular users.

---

## Build 45 (v1.0.1 — April 2026)

**Your coach waits for you to lift before logging.**

The AI was occasionally logging a set as soon as you told it your plan — before you actually lifted. It'll now ask you to complete the set first, then log it once you confirm. Less frustrating, more accurate.

Warmup sets are now recognized and labeled automatically. Say "warming up with 135" and the coach logs it with a warmup note rather than treating it like a working set.

Also fixed: a floating "Done" button that was bleeding through the About You form on iOS.

---

## Build 42 (v1.0.1 — April 2026)

**Coach identity redesign progresses behind the flag.**

The sample conversation (WelcomePrimer) renders with the new coach identity bubble styles so it matches the live chat. Round accent-colored send button with the Lucide paper-plane icon. Scroll-to-latest button added to History. Larger avatar (48px) and refined bubble typography.

---

## Build 41 (v1.0.1 — April 2026)

**Coach identity redesign in progress.**

We've been prototyping a coach identity redesign (new chat bubbles, set cards, session header, tab bar tint) behind a dev flag. Nothing visible to you yet unless you're on the dev allowlist — we'll flip it on for everyone in an upcoming build after testing.

---

## Build 40 (v1.0.1 — April 2026)

**Workout rotation now rotates.**

Fixed a bug where the app would keep recommending the same workout type over and over if you picked the same one a few times in a row. The rotation learner was inadvertently treating "push followed by push" as a pattern and reinforcing it. Now it falls back to the default push → pull → lower rotation whenever it detects that kind of self-reinforcing loop.

---

## Build 39 (v1.0.1 — April 2026)

**Profile data now stays in sync.**

Fixed a bug where your profile fields (weight, goals, injuries) could show up blank after a reinstall or when switching devices — the app was reading a stale local cache instead of pulling fresh data from the server. Your profile now loads correctly every time you open Settings.

Under the hood: the release pipeline now catches TestFlight upload failures properly so we can't accidentally ship a "successful" build that never made it to Apple.

---

## Build 37 (April 2026)

**Explore the full app before you decide.**

When you open Jacked now, you see the whole app — tabs, example history, coach selection, profile — and you can browse first.

New touches:
- Example history cards and stats so you can see what a real session looks like
- Start button wiggles gently when no session is active to draw your eye
- New 4-card onboarding flow that leads with the chat experience

Also: a security fix for account deletion (access-token binding) and a clean-up pass on the Settings footer.

---

## Build 36 (April 2026)

**Workout stats moved to History.**

Workouts, week streak, and average time stats now live on the History screen instead of tucked into Settings — tap any stat card to see details. New icons, cleaner layout, and workout type (PUSH / PULL / LOWER) merged into each history card's date header so you can scan your log faster.

Fixed a streak calculation bug and tightened up the sign-out button styling.

---

## Build 35 (April 2026)

**Session restore is now rock-solid.**

Closing the app mid-workout no longer loses your conversation. Reopen Jacked and pick up exactly where you left off — your coach still has full context.

---

## Build 34 (April 2026)

**Ask your coach about form anytime.**

Not sure how to do an exercise? Ask — "what's the proper form for Romanian deadlifts?" or "how do I do that again?" Your coach gives you a quick, practical breakdown right in chat.

---

## Build 32 (March 2026)

Improved welcome experience for new users.

---

## Build 31 (March 2026)

**New user onboarding.**

New users now see a quick walkthrough with real examples before their first session — showing how the coach tracks your sets, adjusts weights, and builds on your history.

Also: coach no longer assumes your equipment — asks before logging.

---

## Build 30 (March 2026)

**Better offline handling.**

If your connection drops mid-session, you'll see a clear banner instead of a confusing error. Starting a workout without a connection is now blocked with a friendly message instead of silently failing.

---

## Build 28 (February 2026)

- Exercise names are now highlighted in green in chat — easier to scan your session at a glance
- Your current exercise shows in the session bar at the top of the screen

---

## Build 26 (February 2026)

Bug fixes and stability improvements.

---

## Build 24 (January 2026)

Fixed account deletion flow. Minor stability improvements.

---

## Build 23 (January 2026)

- **Rest timer overhaul** — cleaner UI, easier to read your recovery time between sets
- **Account deletion** — you can now fully delete your account from Settings (required by App Store guidelines)
- **Seamless cloud restore** — when you sign in on a new device, your workout history restores automatically in the background

---

## Build 22 (January 2026)

- Rest timer now tracks your recovery between sets
- Bug fixes across the app

---

## Build 21 (January 2026)

**Better session endings.**

Coach now properly wraps up your workout when you're done — recaps what you hit, flags any PRs, and gives you a clean send-off.

---

## Build 20 (January 2026)

Stability improvements.

---

## Build 19 (January 2026)

Internal build — App Store screenshots.

---

## Build 18 (December 2025)

- Coach now handles your available equipment properly during your first session
- Button animations added throughout the app — small detail, better feel
- Feedback and community links added to Settings
- Coach learns your push/pull/lower rotation from your history

---

## Build 17 (December 2025)

- **Rotating coach tips** — tips now cycle based on your workout count, so they stay relevant the more you train
- History now draws from your last 10 sessions instead of a fixed date window — better context for the coach

---

## Build 15 (December 2025)

Website and onboarding updates.

---

## Build 11 (November 2025)

**New onboarding and coach names.**

New step-by-step onboarding walks you through how the app works before your first session.

Coaches now have names:
- **Biff** — direct, high-energy, no excuses
- **Kelly** — warm, encouraging, genuinely excited about your progress

Tips moved into the Start Workout screen.

---

## Build 10 (November 2025)

- App renamed to **Jacked**
- New app icon
- Dark mode only

---

## Build 9 (November 2025)

- Fixed sign-out getting stuck on error
- Switched to jackedapp.ai domain

---

## Build 7 (November 2025)

- Coach no longer assumes your gender
- Fixed display name and session finish UI bugs

---

## Build 5 (October 2025)

**Beta waitlist.**

Beta waitlist added for new signups.
