---
section_id: The Web
nav_order: 2
title: Servers
---

cloud, internet, web sounds magical
demystify, actual hardware some where

### Static vs. Dynamic Web

Traditionally, web servers acted more or less like a read-only shared folder of files. 
You can think of a website as a folder of files.
Thus, a **static website** is a collection of HTML, CSS, JS, images, and other files that are delivered exactly as they are on the server to users. 
A URL in a static site generally represents a request for an HTML document in a specific file location.

In contrast a **dynamic website** uses a server-side programming language to create pages on the fly when a user makes a request. 
Thus a URL represents a query, rather than an existing document on the server. 
Think of complex sites such as social media, where users are constantly adding more data and there is no "static" documents, but streams of every changing content.
None-the-less, what the server ultimately delivers to your browser is still HTML, CSS, and JS.

In these platforms content, templates, and metadata are usually stored in a database. 
For example, the popular [content management systems](https://en.wikipedia.org/wiki/Content_management_system) [WordPress](https://wordpress.com/) and [Drupal](https://www.drupal.org/) use the scripting language PHP and database MySQL.
This enables complex interactivity such as comments, customized views, user management, and a web-based admin interface.

Of course, all that complexity requires a lot of technical overhead... so static sites are experiencing a [renewed boom](https://www.smashingmagazine.com/2015/11/modern-static-website-generators-next-big-thing/), offering simplicity with:

- much faster performance (caching, low bandwidth, no processing time).
- low hosting requirements (simple web servers, no dependencies).
- no security vulnerabilities.
- easy version control.
