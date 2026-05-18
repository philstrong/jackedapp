# Jacked — Release Notes

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
