# 🪜 How Should We Break Down a Task? — Speaker Prompts + Examples

- **“What’s wrong with a task like ‘Build analytics dashboard’?”**  
  → It’s too vague — doesn’t help us estimate, test, or know when we’re done.  
  🗣 *Example fallback:* “Better: ‘Build API to return active user count,’ ‘Render line chart in admin panel.’”

- **“How do you define when a task is *done*?”**  
  → Should have a clear, testable output.  
  🗣 *Example:* “For API: JSON returns expected fields, test added. For UI: chart renders sample data, layout works.”

- **“Why split tasks by delivery steps instead of tech layers?”**  
  → Helps deliver value earlier and reduce dependencies.  
  🗣 *Example:* “Step 1: API returns mock data. Step 2: UI renders mock chart. Step 3: Connect real data.”

- **“When should we use a spike?”**  
  → When there’s too much uncertainty to estimate confidently.  
  🗣 *Example:* “If we’re not sure what’s in the logs or if we even track that metric — do a spike first.”

- **“Do you create tasks for tests, docs, or cleanup?”**  
  → Yes, and you should — they’re real work, not optional.  
  🗣 *Example:* “Write a separate task for unit tests, or for documenting how the dashboard works.”

---

# 🔍 Why Spike Tasks Matter — Speaker Prompts + Examples

- **“What is a spike task, and why do we need it?”**  
  → A spike is a time-boxed investigation — we use it to explore unknowns before estimating.  
  🗣 *Example:* “We think we have usage data, but it's stored in messy `jsonb` logs. A spike helps us confirm what's usable.”

- **“When should we create a spike?”**  
  → When a task has too many unknowns, or the risk of failure is high.  
  🗣 *Example:* “If we’re unsure whether we even log feature usage, don’t guess — spike it.”

- **“How long should a spike take?”**  
  → It should be short and focused — usually 1 day or less.  
  🗣 *Example:* “We time-boxed a 1-day spike to explore user activity data and came out with clear follow-up tasks.”

- **“What should the outcome of a spike be?”**  
  → It’s not a deliverable — it’s knowledge.  
  🗣 *Example:* “After the spike, we know what’s available, what needs cleanup, and what to estimate properly.”

- **“What happens if we skip the spike?”**  
  → You risk underestimating and getting stuck mid-sprint.  
  🗣 *Example:* “We once skipped it, assumed everything was there, then realized halfway through we had to write migration scripts.”

---

# 🎯 Why Points Can Fail in Small Teams — Speaker Prompts + Examples

- **“Have you ever used story points? Did they work well?”**  
  → In small teams, they often create confusion or inconsistency.  
  🗣 *Example:* “We said this was a ‘3-pointer,’ but no one agreed what 3 points meant.”

- **“Why do story points break down in small teams?”**  
  → Not enough historical data, and small team velocity fluctuates a lot.  
  🗣 *Example:* “One person out sick can drop our ‘velocity’ by 30% — that’s noise, not insight.”

- **“What’s the risk of using points without shared context?”**  
  → People estimate based on hours, others on complexity — no common ground.  
  🗣 *Example:* “Someone thought 5 points = 1 week, someone else thought it was a risky 2-day task.”

- **“What can we do instead?”**  
  → Use hours or day-sized chunks if that feels more natural.  
  🗣 *Example:* “We started using half-day / full-day sizing and focused more on task clarity than point numbers.”

- **“If you still want to use points, how do you make them work?”**  
  → Create shared examples and anchor tasks.  
  🗣 *Example:* “We wrote down: ‘This login task is a 2-pointer,’ so we had a real reference to compare new tasks.”

---

# 🔧 How Should We Code It? — Speaker Prompts + Examples

- **“What’s the first thing you do when implementing a feature?”**  
  → Start with refactoring or reviewing the existing code.  
  🗣 *Example:* “Before building the usage API, we cleaned up the old metrics script and added basic tests — it helped uncover edge cases early.”

- **“Why refactor first?”**  
  → It helps you understand the system, reduce bugs, and add guardrails.  
  🗣 *Example:* “You can’t build clean code on top of a mess — refactoring first makes your job easier, not harder.”

- **“Do we need a design spec or doc for every task?”**  
  → Not always, but for complex features, a 1-pager helps align the team.  
  🗣 *Example:* “We sketched the dashboard API + UI on a doc before writing any code — it saved us 2–3 rounds of rework.”

- **“What about documentation?”**  
  → Small teams don’t need heavy docs — make the code clear instead.  
  🗣 *Example:* “Use good naming, comments where it matters, and keep functions focused — your future self will thank you.”

- **“Why invest in automated tests?”**  
  → They catch regressions and save hours during refactors.  
  🗣 *Example:* “We added a test for usage aggregation — caught a bug the next day when someone changed the query.”

---

# 🌀 How Do We Avoid Mid-Sprint Randomness? — Speaker Prompts + Examples

- **“What kind of things have derailed your sprint before?”**  
  → Unexpected bug, urgent sales ask, vague task that turns out huge  
  🗣 *Example:* “We once added ‘small metrics tweak’ mid-sprint — turned out to need new infra setup and blew up 2 days.”

- **“How do we avoid this kind of disruption?”**

  - **📦 Keep the backlog tight**  
    → Only add well-defined tasks to the sprint  
    🗣 *Example:* “We used to drag in half-baked ideas — now we only sprint what’s clarified.”

  - **📣 Communicate early**  
    → If something feels wrong or bigger than expected, say so early  
    🗣 *Example:* “Someone flagged a vague UI task on day 1 — we paused and rewrote it before wasting time.”

  - **🚫 Don’t bundle tech debt into feature work unless planned**  
    → It’s tempting, but unplanned refactors can throw off timelines  
    🗣 *Example:* “We scoped feature work + refactor together, and it worked. When we didn’t, it always overflowed.”

  - **🧯 Escalate scope creep early**  
    → Adjust the plan instead of powering through  
    🗣 *Example:* “Mid-sprint, we realized the dashboard needed role-based access. We split that into next sprint and shipped what we could.”
