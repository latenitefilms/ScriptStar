# Release Notes

### 1.5.0 (Build 26)

**🎉 Released:**
- 23rd April 2026

**🔨 Improvements:**
This release includes local transcription with downloadable models! You'll find all the changes on the page where you can add `SRT`s and kick off the processing.

To create a **New Transcript** for any clip, whether it's been transcribed by Final Cut Pro already or not, just check the box for that clip in the **New Transcript** column, or click the **New Transcript** column header itself to check that box for all clips.

All transcriptions are local, private, free, and never leave your Mac.

Models include:

- Parakeet v3 (fast, multiple European languages)
- Whisper v3-large (slow, but includes Asian languages like Chinese and Japanese)
- Apple's SpeechTranscriber model that's built in (fast, but not as accurate as the other models, and seemingly the model Final Cut Pro uses natively, with poor multi-language support).

You can choose the model to use in the **Options** panel, and the first time you transcribe, the model will download automatically, displaying a progress bar as it does so.

For the most accurate timing, don't use the built-in transcripts — just re-transcribe with Parakeet. It's fast, and the timing is more accurate than Final Cut Pro's own transcripts.

You shouldn't need to manage these models, but if you try Whisper and find it doesn't work for you, just hold `COMMAND+OPTION` as you choose that option to delete its files.

---

### 1.4.0 (Build 20)

**🎉 Released:**
- Sunday 15th March 2026

**🔨 Improvements:**
- We've improved the error messages for the Open Dialog's and Permission Dialog prompts. Thanks for your feedback FCP Cafe Discord team!
- We've improved the handling of comma-delimited decimals when using in `Point2D` in `FCPXML`. Thanks David Peterson for your genius!
- We now support both Compound Clips and Synchronised Clips (although we still strongly recommend using Multicam clips)! Thanks Bill (from Bill and Ben) and TechMixr!

---

### 1.3.3 (Build 18)

**🎉 Released:**
- Thursday 26th February 2026

**🔨 Improvements:**
- It’s now possible to drag a **Library** or **one or more Events** to ScriptStar. If an Event is dragged, the Library location must be chosen in a following step. This allows users to save processing time in large libraries, and also to avoid `FCPXML` issues related to processing some kinds of clips in other Events.
- This release also adds a **Show Options** button to the page where `SRT`'s can optionally be added. Press this button to choose the conversion mode - **Named Favorites**, **Named Favorites on current Favorite ranges only** or **Notes on Keywords**. Please refer to the online [How to Use](/how-to-use/) page for more information on these modes. Thanks for suggesting Jeff Roy!
- All transcription formats (`CSV`, Word, `PDF`) can now be exported at once with a new button below the individual format choices.  Thanks for suggesting Richard Taylor!

**🐞 Bug Fixes:**
- A bug related to handling of clips at `47.95fps` was fixed in [FCPXMLKit](https://fcp.cafe/latenite/#fcpxmlkit). Thanks for reporting FernKraft!
- A bug related to handling of Point 2D data in FCPXML was fixed in [FCPXMLKit](https://fcp.cafe/latenite/#fcpxmlkit). Thanks for reporting Fernando Gorrotxategi Ugarte!

---

### 1.1.0 (Build 13)

**🎉 Released:**
- Friday 20th February 2026

**🔨 Improvements:**
- If you have existing Favourite ranges on your clips that get imported into ScriptStar, we now convert them to a Keyword Collection called **Favorites ⭐️**.

---

### 1.0.3 (Build 12)

**🎉 Released:**
- Thursday 19th February 2026

**🔨 Improvements:**
- Improvements to progress bars/spinners when importing MASSIVE Final Cut Pro Libraries.

---

### 1.0.2 (Build 11)

**🎉 Released:**
- Wednesday 18th February 2026

**🔨 Improvements:**
- Added a Help Button which opens the website.
- Lowered the macOS Deployment Target to macOS Sequoia 15.6. Thanks for suggesting Scott Simmons!
- Improved the open dialog boxes when using as a Final Cut Pro Workflow Extension. Thanks Robin S. Kurz!

---

### 1.0.1 (Build 10)

**🎉 Released:**
- Sunday 15th February 2026

**🔨 Improvements:**
- SRT files now match filenames as well as clip names.
- Long captions are now split into smaller ones.

**🐞 Bug Fixes:**
- Fixed overlapping ranges.

---

### 1.0.0 (Build 9)

**🎉 Released:**
- Saturday 14th February 2026

This is the first release of **ScriptStar**. Woohoo!
