tasknote
========

The script automatically opens your text editor (defaults to vim) and allows you to edit notes. Upon saving notes, an annotation is added to the task to alert you to the fact that notes exist for that task. The annotation captures the first line of the note file and is updated with every modification to the file.

History
-------
* Original implementation: Alan Bowen
* Update to taskwarrior 2.0: Michael Bobroski
* Context-aware annotations: Bjoern Doebel
* Spaces or other 'special' characters can now be used in the name of notes directory: @AlexCzar

Usage
-----

**Create/Edit Note:**

`tasknote <task_id>`

**View Note:**
	
`tasknote <task_id> v`

Actually, you can type anything after <task_id> that comes to mind: v, view, show, list, cat etc. I left it open since no other features are planned.

Note: This behaviour might change soon (d[elete] will be implemented in addition to v[iew])

Configuration
-------------
Save in a place like /usr/bin and flag as executable with sudo chmod a+x /usr/bin/tasknote.

Be sure to edit the FOLDER var in the script. If it does not exist, you will be asked if you want to create it during the first run.

You can also configure the EDITOR (default: vim), VIEWER (default: cat), as well as NOTEMSG, the annotation message appended to the task in taskwarrior.
