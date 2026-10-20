You'll see files ending in `.base` in `00 Meta/Bases`. You don't need to open them to use the vault, but here's what they are.

## In plain words

A base is a **saved search that displays as a table or a board**. It doesn't store any notes. Instead, it looks through your notes, picks out the ones that match some rules, and shows their properties as rows or cards.

> **Think of it like a smart spreadsheet that fills itself in.** Write a note with `course: [[MG472]]` and `type: Lecture`, and it appears in the MG472 Classes table automatically.

It also works in reverse: when you edit a cell in the table or drag a card on a board, the base writes the change into that note's properties.

## How the dashboards use them

One base file can hold several **views** (different tables and boards). For example, `Module Notes.base` holds 🗓️ Classes, 🧠 Understanding board, 🔁 Revise next, 🎯 Deadlines and more.

A dashboard shows a view by embedding it, with a line like:

```
![[Module Notes.base#🗓️ Classes]]
```

Every module dashboard embeds the same views from the same base, and each one only shows its own module's notes. That's why the bases are shared, and why copying a dashboard is all it takes to set up a new module.

## The bases in this vault

| Base | What it powers |
| --- | --- |
| `Module Notes.base` | Everything on each module dashboard |
| `Uni Overview.base` | Deadlines, this week, weak spots and notes to write up, across all modules |
| `Concepts.base` | The 💡 Concepts Dashboard |
| `Literature.base` | The 📖 Literature Dashboard |
| `Job Hunt.base` | The 💼 Job Hunt Dashboard |
| `Books.base` | The 📚 Books Dashboard |

## Should I edit them?

> [!WARNING]
> Please don't edit the files in `00 Meta/Bases`. A change there affects every dashboard that uses it, and template updates replace this whole folder, so your changes would be lost.

This includes small changes made from a table's toolbar, like resizing columns or changing the sort order. Those are saved into the base file too, so they'll reset when you update. That's harmless, just good to know.

## Making your own base

If you want your own table or board, for example of all your MG481 cases, make a new base:

1. Make a folder outside `00 Meta`, e.g. `My bases`.
2. Right-click it, choose **New base**, and give it a name.
3. Use the buttons at the top of the base to choose which notes it shows (**Filter**), which columns appear (**Properties**), and whether it's a table or a board.

Keep your own bases out of `00 Meta/Bases`, because updates replace that folder.

---

⬅️ Previous: [12 Adding a new module](12%20Adding%20a%20new%20module.md) · [📘 Contents](00%20Start%20here.md) · Next: [14 Plugins included](14%20Plugins%20included.md) ➡️
