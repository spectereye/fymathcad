# FyMathcad

FyMathcad is a free Windows utility that provides productivity tools for PTC Mathcad Prime.

The first included tool is a Table of Contents generator for Mathcad worksheets.

![FyMathcad screenshot](screenshots/screenshot.png)

## Privacy and Security

FyMathCAD runs locally on your computer and does not require an Internet connection.

* Mathcad worksheets are processed locally and are not uploaded anywhere.
* FyMathCAD does not collect telemetry or usage data.
* Internet access can be blocked with Windows Firewall without affecting TOC functionality.
* A timestamped backup is created before a worksheet is modified.
* Release binaries are scanned with VirusTotal.
* SHA-256 hashes are published with each release so downloaded files can be verified.

See the corresponding GitHub Release for the VirusTotal report and SHA-256 checksum.

### Windows SmartScreen Notice

FyMathCAD is currently distributed as an unsigned freeware application.
When you run FyMathCAD for the first time after downloading it, Windows may display:

> Windows protected your PC
> Microsoft Defender SmartScreen prevented an unrecognized app from starting.

This warning is expected for a new, unsigned Windows application and does not by itself mean that the application contains malware.
If you downloaded FyMathCAD from the official GitHub Releases page and want to continue:

1. Click **More info**.
2. Verify that the application is `MathcadTOC.exe`.
3. Click **Run anyway**.

## Features

### Preview headings

Open your saved worksheet in Mathcad Prime and make it active, then run **Print chapters**.

FyMathcad lists the saved level-1 headings and their page numbers in the application output.
The list also includes a `=== START ===` entry representing the beginning of the worksheet.

Previewing does not modify, save, close, or reopen the worksheet.

**Unsaved changes are not included.** Save the worksheet in Mathcad Prime first
if you want to preview your latest edits.

### Insert table of contents

Run **Insert TOC** to insert or replace the recognized table of contents,
renumber recognized heading captions, and adjust the layout and page numbers.

The generated TOC includes level-1 headings, with clickable links to the corresponding headings.

**The worksheet is modified in place.**

Before replacing the worksheet, FyMathcad validates the prepared file and
creates a timestamped backup in a `__backup` folder beside the original worksheet.
The backup location is shown in the application output.

The active worksheet is selected at the start of each graphical action.

When **Insert TOC** is run, FyMathcad saves any unsaved changes and closes the worksheet before editing it.
After processing, it attempts to reopen the worksheet even if TOC insertion fails.

Untitled worksheets must first be saved as `.mcdx` files in Mathcad Prime.

## Troubleshooting

* **No headings found:** Use Mathcad heading styles for level-1 headings.
  Visually prominent text alone may not be recognized as a heading.
* **Cannot connect to the worksheet:** Open Mathcad Prime, make the worksheet active,
  and save it as an `.mcdx` file before retrying.
* **Worksheet does not reopen:** Open it manually in Mathcad Prime.
* **Unexpected results:** Review the worksheet layout and page numbers after TOC insertion.
  To restore a backup, close the worksheet and copy the desired timestamped file
  from the `__backup` folder to the original location and filename, replacing the modified worksheet.

## License

Freeware for personal and commercial use.

Copyright © 2026 spectereye@gmail.com. All rights reserved.

See `LICENSE` for license terms.

## Updates

For updates and more engineering tools, visit:

https://biggg.fun/App/FyMathcad
