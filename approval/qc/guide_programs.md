# SYNOPSIS

There are many different ways you can get started coding as there are lots of
programs out there nowadays to use. Below is a guide on how to get started
with the recommended setup of having an FTP client and offline code editor,
so that you can edit files in a modern editor and then upload them via FTP to
Ancient Anguish, rather than trying to use the cumbersome in-game editor.

---

## DESCRIPTION

The first few steps outline how to download and setup the FTP client and the
offline code editor, and then in the later half it discusses some tips and
tricks for changing the preferences in the code editor that affect the
formatting of your code.

You can use whichever FTP client and code editor you prefer, but this guide
will focus on FileZilla and Notepad++ since they are popular, and even if you
do not use these two programs most of the settings and preferences still
apply and you should figure out the equivalent settings in whatever program
that you choose to use instead.

---

## EXAMPLE

FTP Step 1: download "FileZilla" and install it.

FTP Step 2: in the toolbar, go to file, then site manager, and add a new site
for Ancient Anguish with the host name "anguish.org" and use port "3001".
Then in the user text box put your wizard's name (all lowercase), and for the
password text box use your in-game wizard password (be aware that passwords
cap at 8 characters). Now you can connect to the Ancient Anguish FTP server
and it will automatically show your personal wizard directory at the location
of /w/wizardname/ and you can now drag and drop files to FileZilla and they
will appear in your directory in-game.

FTP Step 3: in the toolbar, go to edit, then settings, and in "File Types"
look at the "Default transfer type" and select the "Binary" option. This
prevents FileZilla from trying to convert files to different formats as they
are uploaded and downloaded, and works in tandem with the editor step #3 that
is explained later.

Editor Step 1: download "Notepad++" and install it.

Editor Step 2: in the Notepad++ settings, go to preferences and then to
margins/border/edge and change the "Vertical Edge Settings" to be "77" which
will add a line that runs up and down on your pages showing you where the
right margin is so that you don't write code outside of it. You must read
'man guide_formatting' before starting to code, or you will end up having to
fix things later.

Editor Step 3: in the Notepad++ settings, go to preferences and then new
document and change the "Format (Line ending)" to be "Unix (LF)". This is
necessary because carriage returns characters can negatively affect in-game
viewing of code due to the way they are converted.

Editor Step 4: in the Notepad++ settings, go to preferences and then language
and change the "Tab Settings" to be "Tab size: 2" and also select the
"Replace by space" box. This is necessary because tab characters can
negatively affect in-game viewing of code due because the spacing of tab
indents is different in every program, while whitespace is universal.

Editor Trick: in Notepad++ you can quickly eliminate all trailing whitespace
in a document and then save the file by pressing alt+shift+s on the keyboard.

---

## SEE ALSO

- [qc](./qc/README.md)
