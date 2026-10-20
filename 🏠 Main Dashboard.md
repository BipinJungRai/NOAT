---
banner: Manual/images/dashboard-banner.jpg
cssclasses:
  - wide-page
---
**`= dateformat(date(today), "cccc d LLLL")`** · `= choice(date(today) < date("2026-09-28"), "Before term", choice(date(today) <= date("2026-12-11"), "🍁 AT · Week " + (number(dateformat(date(today), "W")) - 39), choice(date(today) < date("2027-01-11"), "🎄 Winter break", choice(date(today) <= date("2027-03-26"), "☃️ WT · Week " + (number(dateformat(date(today), "W")) - 1), choice(date(today) < date("2027-04-26"), "🐣 Spring break", choice(date(today) <= date("2027-06-11"), "🌱 ST · Week " + (number(dateformat(date(today), "W")) - 16), "☀️ Summer"))))))`

> [!tip] 👋 New here? Start with the [[00 Start here|📘 Manual]]
> Pages 01 to 05 take about 15 minutes and show you how everything works.

> [!nav]
> - **🎓 Uni**
>   - [[📚 Modules|📚 All modules]]
>   - [[MG406|MG406 · Research Design]]
>   - [[MG472|MG472 · Socioeconomics]]
>   - [[MG481|MG481 · Org IT]]
>   - [[MG487|MG487 · Innovation & IS]]
>   - [[MG496|MG496 · Study Skills]]
>   - [[My electives|🆕 My electives]]
> - **🧠 Revision**
>   - [[📊 Literature Dashboard|📖 Cases & Readings]]
>   - [[📊 Concepts Dashboard|💡 Concepts]]
>   - [[📚 Modules#🧠 How well I understand each module|📊 Understanding overview]]
>   - [[📚 Modules#🎯 Deadlines|🎯 All deadlines]]
> - **🧭 More**
>   - [[📊 Job Hunt Dashboard|💼 Job Hunt]]
>   - [[📊 Books Dashboard|📚 Books]]
>   - [[00 Start here|📘 Manual]]

---

## ⚡ At a glance
```dataview
TABLE WITHOUT ID
  length(filter(rows, (r) => contains(list("Lecture", "Seminar", "Workshop", "Guest Talk"), r.type) AND !r.understanding)) AS "⚪ Classes to rate",
  length(filter(rows, (r) => r.understanding = "🔴 No clue" OR r.understanding = "🟠 Shaky")) AS "🔁 Weak spots",
  length(filter(rows, (r) => r.progress = "📝 Brief notes")) AS "📝 Notes to write up",
  length(filter(rows, (r) => contains(r.file.tags, "#job-application") AND (r.status = "Not applied" OR !r.status))) AS "📝 Jobs to apply for",
  length(filter(rows, (r) => contains(r.file.tags, "#job-application") AND contains(list("Applied", "Online test", "Interview", "Assessment centre"), r.status))) AS "📨 Applications live"
FROM "01 UNI/01 Modules" OR "01 UNI/02 Concepts" OR "01 UNI/03 Literature" OR "Job Hunt"
GROUP BY true
```

---

## 🎯 Coming up
*[[10 Deadlines|➕ How to add a deadline]]*

> [!todo] 🎓 Uni deadlines
> ![[Uni Overview.base#🎯 Deadlines]]

> [!warning] 💼 Applications closing in the next 2 weeks
> ![[Job Hunt.base#⏰ Closing in 14 days]]

---

## ✅ To-do
*[[11 To-dos|❓ How to use to-dos]]*
```dataview
TASK
FROM -"00 Meta/Templates" AND -"Manual"
WHERE !completed AND (lower(meta(section).subpath) = "todo" OR (due AND due <= date(today) + dur(7 days)))
GROUP BY file.link
```

---

## 🗓️ Last 7 days at uni
*Rate each class while it's fresh: click the Understanding cell.*
![[Uni Overview.base#🗓️ This week]]

> [!danger]- 🔁 Weak spots (🔴 and 🟠 across all modules)
> ![[Uni Overview.base#🔁 Weak spots]]

---

> [!caution]- 🔒 Template file
> This page comes with the template. Updates from GitHub replace it, so any change you make here will be lost. Your own notes are separate files, so they're always safe. See [[15 Updating and what not to edit]].
