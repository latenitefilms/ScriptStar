# Troubleshooting

Apologies in advance if you have any trouble using ScriptStar. Please read this page first, and if the solutions here don't solve your problem, please [post an issue](https://github.com/latenitefilms/scriptstar/issues) on Github and we'll do our best to solve it.

### If ScriptStar has crashed

Sorry! So you can send them to us, please try to find ScriptStar crash reports here:

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

### If your Library fails to export to ScriptStar — `FCPXML` issues

Sometimes Final Cut Pro can output invalid or incomplete data, and this causes issues for ScriptStar.

When you drag a **Library** from the Final Cut Pro **Browser** to ScriptStar, you're dragging `FCPXML` data (as plain text).

You can see this in action if instead of dragging your **Library** to ScriptStar, you drag it to **TextEdit** - you'll see TextEdit populated with `FCPXML` data.

Unfortunately, **Final Cut Pro v12** currently has some known bugs/issues where _sometimes_ it can't actually export a `FCPXML` that it can then import back into itself.

In these cases, Final Cut Pro is incorrectly outputting `FCPXML` data that isn't correct/valid - and is failing it's own Document Type Definition (DTD).

We are tracking this on FCP Cafe:

- [Final Cut Pro mishandles format of PDF files in FCPXML](https://github.com/CommandPost/FCPCafe/issues/523)
- [FCPXML Crash - `FFXMLExporter(TextStyleExport) newTextStylesForAttributedString:registerStyleTo:`](https://github.com/CommandPost/FCPCafe/issues/521)

These issues have also been reported to the Final Cut Pro team.

If you're having issues with ScriptStar, we suggest trying to export a `FCPXML` of your **Library** to your Desktop and then import it into a new Library.

If it fails to export, or fails to import, then sadly, ScriptStar won't work, and we can't change the data that Final Cut Pro is sending to us.

However, some things you can try to work around the issues with FCP's output:

- Create a new Final Cut Pro **Library** and drag all your **Events** from the old Library to the new Library. You can then transcribe these clips and try to process this new Library with ScriptStar.
- Alternatively, if your Library is large or complex, create a new Final Cut Pro **Library** and drag over just the clips you want to process with ScriptStar to the new Library. You can then transcribe these clips and process this new Library with ScriptStar. Finally, you can drag the new Event it makes back into your original Library.
- Replace any `PDF`s in your **Library** with `TIFF`'s or `PNG`'s.
- Select your **Project** in the **Browser**, then hold down `OPTION` and click the `Clip` menubar item. You'll see a previously hidden `Verify and Repair Project` menubar item. You can use this to try and repair your **Projects** if there's corruption.

If you're still having issues, please [post an issue](https://github.com/latenitefilms/scriptstar/issues) on GitHub and we'll get back to you ASAP.
