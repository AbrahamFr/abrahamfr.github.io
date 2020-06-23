---
layout: post
title: Attribute for testing is data-automation
---

Running Selenium scripts to do automated testing of web pages greatly reduces the time it takes to test a web application.  Also, the quality of the tests becomes very high and gets us closer to TDD, Test Driven Development.

But, there is an issue.  The selectors of Selenium need to be HTML elements or attributes and they can be nested.  Furthermore, a developer may need to completely rework the HTML for a new feature or a refactoring; thus breaking the fragile Selenium scripts of the automation suite.  

A solution that has worked well for me is the HTML attribute of “data-automation”.  By beginning with the word “data-”, the browser will ignore the attribute as a custom attribute for this site.  The test creators and the web page developer can use the attribute when an “id” or “name” is difficult to use.  The web page developer is also able to use TypeScript/JavaScript to inject information into the value of the attribute as needed.

What I have observed is that the data-automation attribute becomes the contract between developer and test creator.  When a change to the UI is needed, if the developer sees a data-automation tag, then she knows that this code has Automation Tests on it.  A conversation with the testers needs to happen as part of the design and hand off of the code change.  

If the change is not explained beforehand, the QA Engineer is able to go back to the developer and ask why the data-automation tags were removed or altered.  The developer is then able to either put back the data-automation tags or discuss with the QA Engineer how to do the new testing.

I have also seen QA Engineers add these attributes or be able to request specific data-automation tags be added to the code.  A very helpful situation for all.