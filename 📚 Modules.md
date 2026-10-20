---
cssclasses:
  - wide-page
---
*[[🏠 Main Dashboard|🏠 Home]] · [[📊 Literature Dashboard|📖 Cases & Readings]] · [[📊 Concepts Dashboard|💡 Concepts]] · [[00 Start here|❓ How this works]]* · **`= dateformat(date(today), "cccc d LLLL")`** · `= choice(date(today) < date("2026-09-28"), "Before term", choice(date(today) <= date("2026-12-11"), "🍁 AT · Week " + (number(dateformat(date(today), "W")) - 39), choice(date(today) < date("2027-01-11"), "🎄 Winter break", choice(date(today) <= date("2027-03-26"), "☃️ WT · Week " + (number(dateformat(date(today), "W")) - 1), choice(date(today) < date("2027-04-26"), "🐣 Spring break", choice(date(today) <= date("2027-06-11"), "🌱 ST · Week " + (number(dateformat(date(today), "W")) - 16), "☀️ Summer"))))))`

## 🎯 Deadlines
![[Uni Overview.base#🎯 Deadlines]]

## 🗓️ Last 7 days
![[Uni Overview.base#🗓️ This week]]

## 🧠 How well I understand each module
*Counts of notes at each rating. To re-rate notes, use the board on each module dashboard.*
```dataview
TABLE WITHOUT ID
  key AS "Module",
  length(filter(rows, (r) => r.understanding = "🔴 No clue")) AS "🔴 No clue",
  length(filter(rows, (r) => r.understanding = "🟠 Shaky")) AS "🟠 Shaky",
  length(filter(rows, (r) => r.understanding = "🟡 Getting there")) AS "🟡 Getting there",
  length(filter(rows, (r) => r.understanding = "🟢 Solid")) AS "🟢 Solid",
  length(filter(rows, (r) => !r.understanding)) AS "⚪ Not rated",
  length(filter(rows, (r) => r.progress = "📝 Brief notes")) AS "📝 To write up",
  round(length(filter(rows, (r) => r.understanding = "🟢 Solid")) / length(rows) * 100) + "%" AS "Solid %"
FROM "01 UNI/01 Modules" OR "01 UNI/03 Literature"
WHERE course AND type != "Assessment" AND type != "Deadline" AND !contains(tags, "MOC") AND !contains(tags, "synthesis")
GROUP BY course
SORT key ASC
```

> [!danger] 🔁 Weak spots (🔴 and 🟠 across all modules)
> ![[Uni Overview.base#🔁 Weak spots]]

### ✍️ Notes still to write up
![[Uni Overview.base#✍️ To write up]]

---
##  🍁 Autumn Term
*Mon 28 Sep to Fri 11 Dec 2026 · 11 teaching weeks · Reading week: Week 6 (w/c 2 Nov)*

| Module                                                              | Code  | Assessment type                                  | Due                                                       | Credit | Lecturer                                      |
| ------------------------------------------------------------------- | ----- | ------------------------------------------------ | --------------------------------------------------------- | ------ | --------------------------------------------- |
| [[MG406\|Research Design for Studies in Digital Innovation]]        | MG406 | Research proposal (100%)                         | TBC (see Moodle)                                          | 0.5    | Anuschka Schmitt (convenor), plus ISI faculty |
| [[MG472\|Management and Socioeconomics of Digital Innovation]]      | MG472 | Exam, 180 min (100%)                             | ST exam period                                            | 0.5    | Dr Antonio Cordella                           |
| [[MG481\|Innovating Organisational IT]]                             | MG481 | Group sprint project (50%) + Exam, 120 min (50%) | Project: AT Week 6 (w/c 2 Nov 2026); Exam: ST exam period | 0.5    | Dr William Venters                            |
| [[MG487\|Innovation and Information Systems]]                       | MG487 | Essay, 3000 words (50%) + Exam, 120 min (50%)    | Essay: TBC (see Moodle); Exam: ST exam period             | 0.5    | Dr Tomislav Karacic                           |
| [[MG496\|Study Skills and Contemporary Topics]]                     | MG496 | Not formally assessed                            | n/a                                                       | 0      | Dr Antonio Cordella                           |

---
## ☃️ Winter Term
*Mon 11 Jan to Fri 26 Mar 2027 · 11 teaching weeks · Reading week: Week 6 (w/c 15 Feb)*

*Your electives come from your own note, [[My electives]]. Edit that note, not this page.*

![[My electives#Winter Term electives]]

> Elective applications: deadline 1pm Mon 11 Jan 2027 (Week 1). Course choice closes 5pm Fri 22 Jan 2027 (Week 2).

---
## 🌱 Spring Term
*Mon 26 Apr to Fri 11 Jun 2027 · 7 teaching weeks · Exam period: Weeks 2 to 7 (w/c 3 May to 11 Jun)*

| Module                                                              | Code  | Assessment type      | Due                        | Credit | Lecturer            |
| ------------------------------------------------------------------- | ----- | -------------------- | -------------------------- | ------ | ------------------- |
| [[MG472\|Management and Socioeconomics of Digital Innovation]]      | MG472 | Exam, 180 min (100%) | ST exam period             | 0.5    | Dr Antonio Cordella |
| [[MG481\|Innovating Organisational IT]]                             | MG481 | Exam, 120 min (50%)  | ST exam period             | 0.5    | Dr William Venters  |
| [[MG487\|Innovation and Information Systems]]                       | MG487 | Exam, 120 min (50%)  | ST exam period             | 0.5    | Dr Tomislav Karacic |
| Dissertation                                                        | MG4D7 | Dissertation (100%)  | TBC (see programme/Moodle) | 0.5    | TBC                 |

---

---

**Total: 2.0 (compulsory) + 1.5 (electives) + 0.5 (dissertation) = 4.0 units**

---

> [!caution]- 🔒 Template file
> This page comes with the template. Updates from GitHub replace it, so any change you make here will be lost. Your own notes are separate files, so they're always safe. See [[15 Updating and what not to edit]].
