From time to time there'll be a new version of the template, with fixes and new features. This page explains how to get it without losing any of your notes.

## Which files are mine, and which are yours?

Every file in the vault belongs to one side. Updates replace the template's files and never touch yours.

| 🔒 Template files (don't edit) | ✏️ Your files (edit freely) |
| --- | --- |
| The `.obsidian` folder (settings and plugins) | Every note you write |
| `00 Meta/Bases` (the tables and boards) | `00 Meta/Attachments` (your screenshots) |
| `Manual` (this manual) | The deadline notes, once you fill them in |
| `🏠 Main Dashboard`, `📚 Modules` | `My electives` |
| The 📊 dashboards (Concepts, Literature, Books, Job Hunt) | Any module you add yourself, including its dashboard |
| The dashboards for MG406, MG472, MG481, MG487, MG496 | Your slides, PDFs and books |

> **The rule:** if a note has a 🔒 **Template file** box at the bottom, don't edit it. Changes you make there will be lost at the next update.

If you want to change how a dashboard works, make your own copy of it first and change the copy.

## Which version do I have?

The version number is at the top of [00 Start here](00%20Start%20here.md). New versions, and what changed in each, are listed on NOAT's GitHub page under **Releases**.

## Updating (if you downloaded the ZIP)

1. **Close Obsidian.**
2. Download the new version: on the GitHub page, click **Code**, then **Download ZIP**, and unzip it.
3. From the new download, **copy these into your vault, replacing the old ones**:
   - the `.obsidian` folder
   - the `00 Meta/Bases` folder
   - the `Manual` folder
   - any other files named in that version's release notes, e.g. `🏠 Main Dashboard.md`
4. Open Obsidian again.

> [!CAUTION]
> Never replace your module folders, `01 UNI/02 Concepts`, `01 UNI/03 Literature`, `00 Meta/Attachments`, `Books` or `Job Hunt`. That's where your own notes are. Replacing a folder deletes everything inside it.

**Can't see the `.obsidian` folder?** It's hidden, because its name starts with a dot.

- **Mac:** in Finder, press `Cmd+Shift+.` (full stop) to show hidden folders.
- **Windows:** in File Explorer, click **View** → **Show** → **Hidden items**.

Replacing `.obsidian` resets any settings you changed yourself, like your theme. You may need to set those again.

## Updating with git

If you got NOAT with git (see [02 Install and set up](02%20Install%20and%20set%20up.md)), updating is one step. In Terminal (Mac) or PowerShell (Windows), go into your NOAT folder and pull the new version:

```
cd ~/Documents/"MISDI Notes"
git pull
```

(Use your own folder name if it's different.)

- Your own notes never cause conflicts, because they're new files that don't exist in the template.
- If you edited a template file, the pull may stop with a conflict. To throw away your change to that file and take the new version, run `git checkout -- "path/to/the file.md"`, then `git pull` again.
- Obsidian rewrites some files in `.obsidian` by itself (e.g. when you change a setting). If those block a pull, run `git checkout -- .obsidian` first. This resets your settings to the template's.
- If you've deleted the example notes and git complains about one of them, bring it back with `git checkout -- "the file name"`, run `git pull` again, then delete it again afterwards.

---

⬅️ Previous: [14 Plugins included](14%20Plugins%20included.md) · [📘 Contents](00%20Start%20here.md) · Next: [16 Troubleshooting](16%20Troubleshooting.md) ➡️
