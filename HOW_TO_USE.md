# Sangam — how to preview and share

## 1. Preview it instantly
1. Unzip the folder.
2. Double-click `index.html` — it opens in your browser and works right away.
3. Go to **Profile** and tap between Citizen / University / Industry / Government to see the app from each side.

Data (challenges, proposals, updates) is saved on your own device via the browser's local storage — good for a demo, but not shared between people yet (see below).

## 2. What's already working
- **Post a challenge** — any role can describe a real problem, tag a domain (environment, health, education, infrastructure, agriculture, water, digital inclusion, safety, livelihoods), and a location.
- **Propose a solution** — University and Industry roles can attach a proposal to any open challenge (approach, org/team name, description). This automatically moves the challenge from *Open* to *In Review*.
- **Government view** — can move any challenge through the full pipeline: Open → In Review → In Progress → Piloted → Solved.
- **Backing / upvoting** a challenge to signal it matters.
- **Explore** — filter challenges by domain, status, or search text.
- **Updates** — a notification feed for new proposals and status changes.
- Accessibility: large-text and high-contrast toggles in Profile.
- Installable as a PWA (Add to Home Screen) with offline caching.
- **Organisation identity** (Profile) — Citizen, University, and Industry roles can each set an organisation name (e.g. an RWA/NGO for citizens, a department for a university, a company name for industry). It replaces the generic role label everywhere that role posts or messages.
- **Role-tailored Home** — University sees open challenges with no university proposal yet; Industry sees active universities it could partner with; Government sees challenges waiting on its review.
- **Private messaging (💬 icon, top right)** — message a specific proposal's organisation directly, or use "Report to government" on any challenge past *Open* status to privately share progress/data with Government. Since there's no real backend yet, switch roles in Profile to reply as "the other side" and see the thread work both ways.
- **Partners directory** (Industry → Profile → "Partner with a university") — lists every university that has proposed a solution so far, with a one-tap "Join & help" message request.
- **Citizen group registration** — a citizen account must register a named group of at least 5 members (Profile → "Register your group") before it can post a challenge or suggestion. This is enforced automatically the first time a citizen tries to post.
- **Suggestions** — a lighter second content type alongside Challenges (Explore has a tab to switch between the two, and "Post" now asks which one you want). A university or industry account can "Take up" an open suggestion, which auto-opens a private chat with the citizen group. Once taken up, either side can privately "Report to government."
- **Government Solution Update** — on any challenge or suggestion, Government can publish an official update: a summary, a work start date, a target/actual end date, and RTI (Right to Information) reference details. This is shown publicly on the item's page for transparency.
- **Camera / photo on posting** — both the challenge and suggestion forms have a "Take / choose photo" button (opens the device camera on mobile, or a file picker on desktop) so a report can include a picture.
- **Tournaments** — when Government notices multiple teams are interested in the same problem, it can turn a challenge into a tournament (Explore → 🏆 Tournaments, or "Start tournament" on any challenge as Government). Set a prize (fast-track adoption or cash), a deadline, and a description. University/Industry accounts submit entries; Government picks a winner with a published reason. The winner's solution auto-closes the linked challenge(s) and publishes a solution update.
- **Solved Library** (Explore → ✅ Solved) — every challenge and suggestion marked Solved lands here permanently as a public, filterable record.

## 3. What's still a placeholder (for real deployment)
- **No accounts yet** — anyone can switch roles freely from Profile. A real launch needs sign-up/login so a university account can't pretend to be a government account, and so a citizen group's identity can't be faked.
- **No shared backend** — right now every visitor's data (including chat messages) lives only on their own device. To make a challenge posted by one person actually visible to a university or company on another device, connect a backend (Firebase is the easiest free option). Come back and ask for this and it can be wired in directly.
- **Photos are stored as-is, uncompressed** — fine for a demo, but a real deployment should compress images before saving to avoid bloating storage.
- **No verification of citizen group members** — the group registration only checks that 5 names were entered, not that those 5 people are real or consented. A production version would want each member to confirm via OTP/email.

## 4. If you want to keep building
Come back to this chat and describe what to change — e.g. "connect Firebase so challenges sync across devices," "add login," or "add a map view to Explore" — and it can be added directly to these files.
