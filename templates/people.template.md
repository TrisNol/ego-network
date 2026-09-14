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
job title: <% await tp.system.prompt("Job title") %>
department: 
teams:
skills:
location: 
status: <% await tp.system.suggester(["Active", "Inactive", "Hiring"],["active", "inactive", "hiring"], false, "What's the current employment status?") %>
URLs:
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
---
