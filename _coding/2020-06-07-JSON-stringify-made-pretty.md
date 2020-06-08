---
layout: post
title: JSON.stringify made pretty
---

I write and debug a lot of TypeScript/JavaScript.  Although, I also do C#.net, T-SQL, Bash, Batch, and Powershell, JavaScript has been a main stay of mine sign 2014.  I have found `JSON.stringify` and `JSON.parse` to be highly valuable tools of the trade.

I often use a [JSON Online Editor](https://jsoneditoronline.org/) as well as the text editor of choice, mine is [VS Code](https://code.visualstudio.com/).  But, in the browser console window, JSON.stringify is king.

I had forgotten that I could pretty up the JSON with a two extra parameters.

`JSON.stringify(objectOrArray, null, 2)`

This allows for the output to be in a more readable format.

Thus, 
`JSON.stringify({"User":{"firstName":"Abraham","lastName":"French"},"blog":"https://abrahamfr.github.io/coding/","gitRepo":"https://github.com/AbrahamFr/angular-router","twitter":"@AbrahamFrench10","linkedIn":"https://www.linkedin.com/in/abrahamfrench/"}, null, 2)`

becomes: 

```JSON
{
  "User": {
    "firstName": "Abraham",
    "lastName": "French"
  },
  "blog": "https://abrahamfr.github.io/coding/",
  "gitRepo": "https://github.com/AbrahamFr/angular-router",
  "twitter": "@AbrahamFrench10",
  "linkedIn": "https://www.linkedin.com/in/abrahamfrench/"
}
```
