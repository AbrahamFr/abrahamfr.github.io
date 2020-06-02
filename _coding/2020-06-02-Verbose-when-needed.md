---
layout: post
title: Verbose when needed
---

There is a tendency to push for the smallest, most compact code at all times.  But, that is a mistake.

1. `!element`
1. `Boolean(element)`
1. `element === null || element === undefined`

Even with ternaries, I use the one that makes sense in context.
1. `const item = element.value || "missing"`
1. `const item = element.value ? element.value : "missing"`


The major idea is that other humans can read and understand the code, not that it is written the best way for a computer or computer science course. Sometimes repeating the code may make the meaning and debugging simpler.

