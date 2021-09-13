---
title: "<% tp.date.now("dddd, MMMM Do YYYY") %>"
---
[[<% tp.date.now("YY-MM-DD_dd", -1) %>]] | [[<% tp.date.now("YY-MM-DD_dd", 1) %>]] 

**Week**: [[<% tp.date.now("gg-MM-[W]ww") %>]]
**Month**: <% tp.date.now("MMMM") %> | [[<% tp.date.now("YY-MM_MMM") %>]]
**Year**: [[<% tp.date.now("YYYY") %>]]

## Daily Notes

----
%% - metadata:
	- tags: #dailies [[Timestamps]] 


	```
aliases: ["<% tp.date.now("MMMM Do, YYYY", 0, tp.file.title, "YYYY.MM.DD") %>","<% tp.date.now("MMMM D, YYYY", 0, tp.file.title, "YYYY.MM.DD") %>","<% tp.date.now("MMM D, YYYY", 0, tp.file.title, "YYYY.MM.DD") %>","<% tp.date.now("MMM. D, YYYY", 0, tp.file.title, "YYYY.MM.DD") %>","<% tp.date.now("M/D/YYYY", 0, tp.file.title, "YYYY.MM.DD") %>","<% tp.date.now("M-D-YYYY", 0, tp.file.title, "YYYY.MM.DD") %>","<% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY.MM.DD") %>","<% tp.date.now("M.D.YYYY", 0, tp.file.title, "YYYY.MM.DD") %>",]
created: ["<% tp.file.creation_date("YYYY.MM.DD h:mm A") %>"]
```