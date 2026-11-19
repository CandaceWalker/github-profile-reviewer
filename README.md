# github-profile-reviewer
An AI agent that helps recruiters read a candidate’s GitHub and ask sharper screen questions.
# GitHub Profile Reviewer 🔎

An AI agent that helps technical recruiters understand what a candidate's public GitHub actually shows, relative to a specific role, and turns it into sharp, specific questions for the screen.

Works with a **Claude Project** or a **Gemini Gem**. No code required.

## Why I built it
A candidate's GitHub can be full of real signal, but it's easy to misread. Stars, followers, and green squares look impressive and say little about skill. Meanwhile, the things that matter, like tests, merged pull requests, and thoughtful project history, are easy to miss if you don't know where to look.

This agent reads a profile the way an experienced technical recruiter would, so I walk into every screen with specific, informed questions about the candidate's actual work.

## What it does
Give it a role profile and a GitHub link. It returns:

| Section | What you get |
|---|---|
| **Relevant to this role** | Specific repos and contributions tied to the role's must-haves |
| **Engineering habits** | Tests, documentation, CI, and commit quality, only what it actually saw |
| **Collaboration** | Contributions to other projects, and whether they were merged |
| **What GitHub doesn't tell us** | Must-haves the public work doesn't show yet |
| **Questions for the screen** | Questions that reference the candidate's actual projects |
| **Summary for the hiring manager** | A neutral, 2–3 sentence summary |

See [`example-review.md`](example-review.md) for a full sample.

## Built-in fairness rules
- **An empty GitHub is never a negative.** Most engineers do their best work in private company repos.
- Ignores names, photos, location, schools, and personal details.
- Doesn't treat stars, followers, or the contribution graph as measures of skill.
- Doesn't penalize gaps in activity.
- Reviews only public GitHub work, nothing about the candidate's personal life.
- Describes evidence. It never scores or ranks people.

## Files
| File | What it's for |
|---|---|
| [`agent-instructions.md`](agent-instructions.md) | Paste once into your Claude Project or Gemini Gem |
| [`role-profile-template.md`](role-profile-template.md) | Fill in for each role |
| [`github-signals-guide.md`](github-signals-guide.md) | A recruiter's guide to reading GitHub, useful on its own |
| [`example-review.md`](example-review.md) | A sample review for a fictional candidate |

## Setup
1. Create a **Claude Project** or **Gemini Gem**.
2. Paste the contents of `agent-instructions.md` into its instructions.
3. Turn on web browsing if your tool has it, so the agent can open GitHub profiles. Without it, paste in repo names and READMEs.
4. Send a filled-in role profile, then one GitHub link at a time.

## Tips
- **Use it to prepare, not to filter.** It's built to make screens better, not to decide who gets one.
- **Verify before you quote.** Open the repos the agent mentions before referencing them with a candidate.
- **Review one candidate at a time,** and only candidates already in your process.

---

📫 [Connect with me on LinkedIn](https://linkedin.com/in/candacerwalker)
