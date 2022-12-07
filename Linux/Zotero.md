# Issue with setting PDF open application
While Zotero uses the system-default PDF reader by default, file handling on Linux can be affected by many settings. If you find that PDFs open in, say, Gimp even though you've set the file handler to be Okular in Dolphin/Nautilus/etc., the easiest solution is to choose a specific PDF reader from the General pane of the Zotero preferences.

If you'd like to keep the setting as “System Default”, you can try the following:

Open the file

```
~/.local/share/applications/defaults.list
```

in a text editor and look for the line “application/pdf=…”. Change it to

```
application/pdf=kde4-okularApplication_pdf.desktop
```

If the file does not exist, create it and enter the following content:

```
[Default Applications]
application/pdf=kde4-okularApplication_pdf.desktop
```

Note: On some systems, you might need to use

```
application/pdf=kde-okularApplication_pdf.desktop
```

instead.

For other PDF readers you might use one of the following:

- `application/pdf=evince.desktop`
- `application/pdf=acroread.desktop`
- `application/pdf=Foxit-Reader.desktop`

[Ref](https://www.zotero.org/support/kb/file_handling_issues#pdfs_opening_in_wrong_application_on_linux_systems)