# Filler Word & AI-Pattern Blacklist

When any of the following are detected — in user-provided text OR in the agent's own draft —
the agent must warn the user, explain the reason, offer a rewrite, and allow the user to
override. Never silently leave a blacklisted item in the final CV.

---

## Category 1: HR/ATS Red Flag Phrases

These are overused to the point that recruiters and ATS systems either ignore or penalise them.

| Banned | Why | Rewrite guidance |
|--------|-----|-----------------|
| passionate about | Meaningless — every candidate says this | Delete. Show passion through achievements instead |
| hardworking | Unverifiable claim | Delete. Results prove work ethic |
| team player | Cliché | Delete or rewrite as a concrete collaboration example |
| results-driven | Claimed, not shown | Delete. Let metrics do this job |
| detail-oriented | Every CV says this | Delete. Let accurate, specific bullets prove it |
| dynamic | Vague positive adjective | Delete |
| proactive | Vague | Delete or rewrite as a specific action taken |
| innovative | Claimed, not shown | Delete or cite a specific innovation |
| go-getter | Informal and cliché | Delete |
| motivated | Meaningless on a CV | Delete |
| self-starter | Cliché | Delete |
| synergy | Corporate filler | Delete |
| thought leader | Almost always unearned | Delete unless citing a publication/keynote |
| guru / ninja / rockstar / wizard | Unprofessional | Replace with actual job title |
| game-changer | Marketing speak | Delete |
| cutting-edge | Vague | Replace with the actual technology name |
| best-of-breed | Marketing speak | Delete |
| holistic | Vague | Be specific about what was considered |
| robust (used vaguely) | Meaningless without context | Describe the actual quality |
| seamless | Vague positive | Describe what was achieved or how |
| proven track record of | Filler opener | Delete — start with the verb directly |
| I bring X years of | Weak opener | Rewrite: "X years of [domain] experience, including..." |
| responsible for | Passive, weak | Rewrite with an action verb |
| in order to | Verbose | Replace with "to" |
| utilize / utilized | Pretentious version of "use" | Replace with "use" / "used" |
| leverage / leveraged | Overused business speak | Replace with "used", "applied", or "built on" |
| spearheaded | Corporate cliché | Replace with "Led", "Built", "Launched" |

---

## Category 2: AI-Writing Patterns

These patterns are strongly associated with AI-generated text. Recruiters and hiring managers
are increasingly trained to spot them.

| Pattern | Example | Why it's a problem |
|---------|---------|-------------------|
| Mid-phrase em-dash clause | "a results-driven approach — delivering outcomes" | AI signature pattern |
| "not only...but also" | "not only built the model but also deployed it" | AI connector phrase |
| "in today's fast-paced world" | any usage | Pure AI filler |
| "I am excited to" | any usage | AI cover letter filler — never in a CV |
| "I am passionate about" | any usage | AI filler |
| Bullets starting with "I" | "I developed a pipeline..." | CVs use implied subject — no "I" |
| Emojis | 🚀 📊 ✅ | Never appropriate in a professional CV |
| Oxford comma overuse | "Python, SQL, and, additionally, R" | AI over-punctuates |
| Hyphens connecting unrelated clauses | "data-driven — insights-focused — outcome-oriented" | AI structure(this is critical) |
| Repetitive sentence structure | Every bullet starts the same way | Sign of templated output |
| Generic superlatives | "exceptional", "outstanding", "remarkable" | AI self-praise |
| "various" | "various stakeholders", "various tools" | Vague — name them specifically |
| "etc." at end of lists | "Python, SQL, Power BI, etc." | Unprofessional — be complete |

---

## Category 3: Structural Anti-Patterns

These are formatting or structural choices that harm ATS parsing or human readability.

| Anti-pattern | Why it fails | Fix |
|-------------|-------------|-----|
| Skills rating bars (1-5 stars) | ATS cannot parse them; looks junior | Plain text keyword list |
| Coloured text or backgrounds | Some ATS strip colour; looks gimmicky | Black text only |
| Profile photo | Illegal bias risk in many countries; ATS ignores images | Remove |
| Tables for layout | ATS often misreads table cells | Use LaTeX itemize + spacing |
| Icons/symbols in skills section | ATS cannot parse | Plain text only |
| Objective statement ("I am looking for...") | Outdated — replaced by Professional Summary | Remove |
| References available on request | Wastes space — assumed by default | Remove |
| Salary expectations | Never on a CV | Remove |
| Hobbies/Interests | Rarely adds value; takes space | Only include if directly relevant |
| Header/footer for key contact info | Some ATS skip headers/footers | Keep all contact info in body |

---

## Warning Output Format

When the agent detects a blacklisted item, it must output:

> ⚠️ **Flagged:** "[exact phrase found]"
> **Why this is a problem:** [one sentence explanation]
> **My suggested rewrite:** "[replacement text]"
> **Your choice:** Keep my rewrite / provide your own / override and keep original

The agent then waits for the user's response before finalising that section.
