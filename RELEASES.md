# Jacked — Release Notes

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

The paywall has moved from app entry to workout start. When you open Jacked now, you see the whole app — tabs, example history, coach selection, profile — and the paywall only appears when you tap Start on a workout. Browse first, decide later.

New touches:
- Example history cards and stats so you can see what a real session looks like before you pay
- Orange "Get Jacked" button at the top of every screen if you want to subscribe from anywhere
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

## Build 29 (March 2026)

Fixed a bug where switching accounts could carry over subscription state from the previous user.

---

## Build 28 (February 2026)

- Exercise names are now highlighted in green in chat — easier to scan your session at a glance
- Your current exercise shows in the session bar at the top of the screen
- Subscription status now loads correctly even when you're offline

---

## Build 27 (February 2026)

Fixed yearly subscription plan not activating correctly after purchase.

---

## Build 26 (February 2026)

Bug fixes and stability improvements.

---

## Build 25 (February 2026)

Added Privacy Policy and Terms of Use links to the subscription screen.

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
- Fixed price display overflow on the subscription screen

---

## Build 8 (November 2025)

**Subscriptions live.** Payments fully enabled for new users.

---

## Build 7 (November 2025)

- Coach no longer assumes your gender
- Fixed display name and session finish UI bugs

---

## Build 5 (October 2025)

**Beta waitlist.**

Beta waitlist added for new signups.
