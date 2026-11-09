from pathlib import Path

source = Path("/mnt/data/Pasted text(20261109-054920).txt")
readme = source.read_text(encoding="utf-8")

insert = r"""
---

# 🧪 Beyond the Usual Projects

I enjoy building technology that solves practical problems, not just completing tutorials.

## 🎓 DishaSetu — Student Career Platform

A platform concept focused on connecting students with job and internship opportunities.

- Student job and internship discovery
- Application status tracking
- Corporate job management
- Offer-letter upload and viewing
- Student profile and application details

`React` `TypeScript` `Python` `PostgreSQL`

## 🦺 SafetySync Pro — Workplace Safety Platform

A safety-focused platform concept for improving HSE reporting and workplace awareness.

- Incident reporting and tracking
- Training and meeting records
- Rectification workflows
- Good-practice reporting
- Smart photo intelligence and incident heatmaps

`React` `Node.js` `AI/ML`

## 💧 AquaFlow — Water Supply Management

A water-supply project where I worked on the frontend experience.

- User-friendly interface
- Clear water-service information
- Responsive frontend design

`Frontend Development` `JavaScript` `HTML` `CSS`

---

# 🧠 How I Approach Development

```text
Understand the problem
        ↓
Plan the solution
        ↓
Build and test
        ↓
Learn from mistakes
        ↓
Improve and ship
```

I believe good development is not about writing the most code.
It's about building something useful, reliable, and easy to use.

---

# 🤝 Open to Collaboration

I'm interested in collaborating on:

- Full-stack web applications
- Backend APIs and database-driven projects
- AI/ML experiments
- Student-led and hackathon projects
- Open-source contributions

If you're building something interesting, let's connect and create something meaningful.

---

"""

marker = "# 📊 GitHub Stats"
if "## 🧪 Beyond the Usual Projects" not in readme and marker in readme:
    readme = readme.replace(marker, insert + marker, 1)

# Save a clean Markdown README while retaining the original content and image paths.
output = Path("/mnt/data/README_Aman_Upgraded.md")
output.write_text(readme, encoding="utf-8")

print(f"Created: {output.name}")
print(f"Lines: {len(readme.splitlines())}")
print("Added sections: Beyond the Usual Projects, How I Approach Development, Open to Collaboration")
