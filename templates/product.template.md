---
<%* 
	let title = tp.file.title; 
	if (title.startsWith("Untitled")) { 
		title = await tp.system.prompt("Enter document title"); 
		await tp.file.rename(title); 
	}
-%>
aliases:
tags:
tech stack:
deployment:
visibility:
URLs:
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
