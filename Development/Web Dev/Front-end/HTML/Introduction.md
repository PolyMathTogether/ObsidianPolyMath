Have you ever thought about "how is a website **structured**"? It also has a **skeleton structure** like us and is written entirely in a language. That is **HTML** or **Hypertext Markdown Language**. It is interpreted by our browser such as Chrome, Firefox then converts into a visual web page. 

# History
---
**HTML** was initially invented and developed by [Tim Berners-Lee](https://en.wikipedia.org/wiki/Tim_Berners-Lee) in 1991. Its first version was __very simple__ but it allowed user to create a webpage to display on _any web browsers_. Overtime, it gradually became more complicated. The newest version is HTML5.

## Time line

| **Versions** | **Release Year** | **Main Features**                               |
| ------------ | ---------------: | ----------------------------------------------- |
| HTML 1.0     |             1991 | basic elements and attributes                   |
| HTML 2.0     |             1995 | image, table, form                              |
| HTML 3.2     |             1997 | multi-media, script, CSS                        |
| HTML 4.01    |             1999 | the last version before being replaced by XHTML |
| XHTML 1.0    |             2000 | higher consistency                              |
| HTML5        |             2014 | the latest version.                             |

# How it works?
---
When a webpage is loaded, your browser recieves an HTML document from the server. This document is read by our browser then interpreted its HTML elements to JS objects called **Node**. Eventually, we have a tree structured model known as **DOM (Document Object Model)**. The same with CSS styles, we have **CSSOM (CSS Object Model)** tree. 

The DOM and CSSOM are combined to form the **render tree**. Each node in this tree has content and styling. Also, it must be "visible" node. For calculating the position and dimensions of each node, the **layout** will take this role. 

The final stage is called **painting** which uses informations from above such as visible nodes, styles, etc... and converts it into pixels on our screen.

