# splitPhorge

A lightweight, non-destructive Python command-line utility that splits Markdown documents into smaller files based on specified heading levels.

## Features

- **Customizable Splitting & Conversion:** Choose exactly which header level to split your document by (H1 through H6). You can also optionally convert the targeted split headers to a different level upon export (e.g., split by H3 but save the new files starting with H1), leaving all nested sub-headers completely intact.
- **Dual Export Modes:**
  - **Individual Files:** Creates a separate Markdown file for every single header.
  - **A-Z Grouping:** Compiles sections alphabetically into `A.md`, `B.md`, etc., based on the first letter of the header. It also neatly groups numbered headers into files like `1.md` and symbols into a `Misc.md` file. It will auto-populate missing alphabetical letters (A-Z) with placeholder text to ensure your glossary is complete!
- **Smart Naming & Formatting:** Automatically names the newly generated Markdown files using the text of the corresponding headings. Spaces in all generated filenames (including prefixes) are automatically replaced with underscores (`_`).
- **Custom Prefixes:** Optionally add a custom prefix (like `Magic_Spells_`) to bulk-rename all exported files instantly.
- **Continuous Workflow:** The app loops, asking if you have another file to split, so you can process multiple documents in one session.
- **Visual Reporting:** Provides real-time console feedback as each file is created, plus a summary of the total sections processed at the end.
- **Non-Destructive & Clean:** Your original source file is never altered or deleted. The app also strictly trims excess blank lines to ensure your exported Markdown formatting is perfectly flush.
- **Organized Output:** Automatically creates an `Exported Files` folder to keep your working directory clean.
- **Robust:** Easily handles large files (even those with over 10000 lines of text) and seamlessly copies complex Markdown elements like tables, nested lists, code blocks, and images.

## Prerequisites

- Python 3.x installed on your system. No external libraries are required.

## Usage

1. Place the `splitPhorge.py` script in the exact same folder (directory) as the Markdown file you wish to split.

2. Open your terminal or command prompt and navigate to that folder.

3. Run the script using Python:

   ```
   python splitPhorge.py
   ```

4. Follow the interactive prompts:

   - **Filename:** Enter the name of your file (e.g., `my_document.md`). The app will auto-append `.md` if you happen to forget it.
   - **Header Level:** Enter the level you want to split by (e.g., `H1`, `H2`, `H3`). Pressing `Enter` without typing anything will automatically default to `H1`.
   - **Target Header Level:** Enter the new level you want the split headers to be converted to (e.g., `H1`), or press `Enter` to leave them as they are.
   - **Export Type:** Choose `1` for Individual files or `2` for an alphabetized A-Z export.
   - **Prefix:** Add a prefix for the exported files or press `Enter` to skip.
   - **Continue:** When the split is complete, type `y` to process another document, or `n` to quit.

---

**License**

issuePhorge is licensed under the GNU General Public License v3.0 (GPL-3.0). This means you can freely use, modify, and distribute this software, provided that:

- You disclose the source code of your modifications
- You license your modifications under the same GPL-3.0 license
- You preserve the original copyright notices and disclaimers
- See the LICENSE file for the complete text of the GPL-3.0 license.