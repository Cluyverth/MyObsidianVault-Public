---
tags: []
cssclasses:
  - dash
  - dashboard
aliases:
---
### Statistics
> [!LifeData]+ Vault Data
> 🗃️ `$=dv.pages().length` **Vault Notes**
> ⏳`$=dv.pages('#Note/Fleeting').length` **Fleeting Notes**
>🎴`$=dv.pages('#ExcelsiorSeguros/Cobrança/Backlog/Card').length` **Backlog Card Cobrança**
> 🧭 `$=dv.pages('"Atlas/Notes"').length` **Atlas Notes**
> 🗓️ `$=dv.pages('"Calendar/Notes"').length` **Calendar Notes**
>  🌡️ `$=dv.pages('"Efforts/Notes"').length` **Effort Notes**
> 🗺️ `$=dv.pages('"Atlas/MOCs"').length` **MOCs**
> ⚙️ `$=dv.pages('"Settigns/Templates"').length` **Templates**
### Tree of Knowledge
> [!TreeofKnowledge]+ Tree of Knowledge
> ```dataview
> LIST
>FROM #MOC  
>SORT file.name ASC
>```
### Tasks
>[!TasksManager]+  Work Tasks
>```tasks
>not done
>heading includes Work
>path does not include Templates
>```
### Fleeting Notes

> [!LifeData]+ Fleeting Notes 
>```dataview
>LIST
>FROM #Note/Fleeting 
>WHERE file.name != "Fleeting_Note_Template"
>SORT file.name ASC
>```
### Efforts
- ### 🔥In-progress
	```dataview
	LIST
	FROM "Efforts/Notes"
	WHERE Status = "In-progress"
	SORT file.name ASC
	```
- ### 🌡️Scheduled
	```dataview
	LIST
	FROM "Efforts/Notes"
	WHERE Status = "Scheduled"
	SORT file.name ASC
	```
- ### 💤Sleeping
	```dataview
	LIST
	FROM "Efforts/Notes"
	WHERE Status = "Sleeping"
	SORT file.name ASC
	```
- ### ✅Done
	```dataview
	LIST
	FROM "Efforts/Notes"
	WHERE Status = "Done"
	SORT file.name ASC
	```