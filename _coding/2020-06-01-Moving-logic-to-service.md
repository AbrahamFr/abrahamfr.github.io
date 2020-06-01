---
layout: post
title: Moving logic into Services
---

Instead of putting logic and structures directly into a component, function, or class, I find it best to begin with moving those structures whether as : 
* struct
* type
* data type
* mock data
* initial data
* discrete logic 
* call to database
* call to third party
* storing data in cookies, session, or local storage

In all these cases, I find it better to have code moved away from the nexus of the component.
