# Troubleshooting

### ScriptStar has crashed

You can find any crash reports here:

`/Users/YOUR-USER-NAME/Library/Logs/DiagnosticReports`

You can also copy the below path, press **COMMAND+SHIFT+G** from Finder (or via the **Go > Go to Folder...** menubar item), and paste in that path into the **Go to Folder** popup:

```
~/Library/Logs/DiagnosticReports
```

Any crashes related to ScriptStar will have **ScriptStar** at the start of the filename.

There might also be crash logs in the **Retired** sub-folder (these are crash logs that have already been sent to Apple):

`/Users/YOUR-USER-NAME/Library/Logs/DiagnosticReports/Retired`

Please `ZIP` up all of these individual crash logs, so that we can review them all.

You [post an issue](https://github.com/latenitefilms/scriptstar/issues) with these files in a `ZIP`, and we'll try and resolve your specific problem.

---

### `FCPXML` issues

When you drag a **Library** from the Final Cut Pro **Browser** to ScriptStar, you're dragging `FCPXML` data (as plain text).

You can see this in action if instead of dragging your **Library** to ScriptStar, you drag it to **TextEdit** - you'll see TextEdit populated with `FCPXML` data.

Unfortunately, **Final Cut Pro v12** currently has some known bugs/issues where it can't actually export a `FCPXML` that it can then import back into itself.

Final Cut Pro is incorrectly outputting `FCPXML` data that isn't correct/valid - and is failing it's own Document Type Definition (DTD).

We are tracking this on FCP Cafe:

- [Final Cut Pro mishandles format of PDF files in FCPXML](https://github.com/CommandPost/FCPCafe/issues/523)
- [FCPXML Crash - `FFXMLExporter(TextStyleExport) newTextStylesForAttributedString:registerStyleTo:`](https://github.com/CommandPost/FCPCafe/issues/521)

These issues have been reported to the Final Cut Pro team.

Sadly, when Final Cut Pro outputs bad data, there's not much we can do about it.

If you're having issues with ScriptStar, we suggest trying to export a `FCPXML` of your **Library** to your Desktop and then import it into a new Library.

If it fails to export, or fails to import, then sadly, ScriptStar won't work.

Things you can try to fix Final Cut Pro:

- Create a new Final Cut Pro **Library** and drag all your **Events** from the old Library to the new Library.
- Replace any `PDF`s in your **Library** with `TIFF`'s or `PNG`'s.
- Select your **Project** in the **Browser**, then hold down `OPTION` and click the `Clip` menubar item. You'll see a previously hidden `Verify and Repair Project` menubar item. You can use this to try and repair your **Projects** if there's corruption.

If you're still having issues, please [post an issue](https://github.com/latenitefilms/scriptstar/issues) on GitHub and we'll get back to you ASAP.