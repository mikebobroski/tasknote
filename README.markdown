tasknote
========

The tasknote script was originally written by Alan Bowen and updated by Michael Bobroski to work with taskwarrior 2. He also added the ability to quickly view a note instead of opening it up in an editor.

I modified the way tasknotes are presented as annotations: after modifying a note, the note file's first line is attached to the task as an annotation. Previous [tasknote] annotations are removed.

The script automatically opens your text editor (defaults to vim) and allows you to edit notes. Upon saving notes, an annotation is added to the task to alert you to the fact that notes exist for that task.


Usage
-----

**Create/Edit Note:**

`tasknote <task_id>`

**View Note:**
	
`tasknote <task_id> v`

Actually, you can type anything after <task_id> that comes to mind: v, view, show, list, cat etc. I left it open since no other features are planned.

Configuration
-------------
Save in a place like /usr/bin and flag as executable with sudo chmod a+x /usr/bin/tasknote.

Be sure to edit the FOLDER var in the script. If it does not exist, you will be asked if you want to create it during the first run.

You can also configure the EDITOR (default: vim), VIEWER (default: cat), as well as NOTEMSG, the annotation message appended to the task in taskwarrior.
