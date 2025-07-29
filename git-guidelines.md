
# Git general guidelines

As a development team:

* We aim to **collaborate smoothly** and **move fast without breaking things**.

* We use **clear branch names** and **well-written commits** to make our history easy to read and understand.

* We **enforce consistency** through naming conventions and commit rules.

* We integrate tools like **Commitlint** and **Conventional Commits** to **automate good practices**.

* We believe **Git history is for humans**, not just machines.

To do so, we write down some guidelines that could be useful.

---

## Branch naming convention

> We use **clear branch names** to keep things organized and easy to follow.

Naming your branch properly makes it easier for others (and your future self) to understand what you're working on — without opening Jira or reading your 42 commits.

Use this format:

```
<type>/<jira-id>-<short-description>
```

Examples:
```
feat/PROJ-123-login-endpoint
fix/PROJ-456-null-checks
chore/PROJ-789-update-ci
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `chore`: Configuration, CI/CD, etc.
- `refactor`, `docs`, `test`, etc. (same as commit types)

> This tiny habit brings huge clarity to PR reviews and Git logs.

![Branch naming](./img/git-branch-naming.png "Branch naming")

---

## Conventional commits

> We write commits that tell a story — short, clear and consistent.

The [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) format helps automate changelogs, releases and Git history analysis.

Use this format:

```
<type>(optional-scope): short description
```

Examples:
```
feat(auth): add token refresh logic
fix(core): prevent crash when API returns null
docs: update README usage instructions
```

**Types we use:**
- `feat`, `fix`, `refactor`, `docs`, `chore`, `test`, `ci`, `perf`, `style`

💡 *Avoid "misc changes", "oops", or "try again" — your teammates deserve better.*

![Conventional commit](./img/conventional-commit.png "Conventional commit")

---

## Commitlint & IntelliJ plugin

> We integrate **tools** to **make good practices automatic**.

### ✅ IntelliJ – Conventional Commit Plugin

- Adds a small UI when committing
- Shows available commit types and scopes
- Prevents you from writing “useless” messages like `“changes”`

📍To install:
```
Settings → Plugins → Marketplace → Search "Conventional Commit"
```
---

## Why this matters

> We believe **Git history is for humans** — and should be readable, traceable and reliable.

Clean Git practices bring clarity in PR reviews, help you squash bugs faster, and make onboarding new teammates a breeze.

![Git is for humans](./img/git-is-for-humans.jpg "Git is for humans")

---

## Summary

| 🔧 Practice         | 💡 Example                             |
|---------------------|----------------------------------------|
| **Branch naming**   | `feat/PROJ-101-login-form`             |
| **Commit format**   | `fix(core): avoid crash when input is empty` |
| **Enforced with**   | Commitlint + Conventional Commit plugin |
| **Bonus**           | Easy changelogs, faster reviews, cleaner diffs |

---

## Final thought

Git is our timeline. Let’s make it clean, clear, and human-friendly.  
Future-you (and your team) will thank you. 🙌
