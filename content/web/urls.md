---
section: Servers
nav_order: 2
title: Addresses
---

To get what we want from a server, we use a web address, that is a Uniform Resource Locator, <span class="term">URL</span>.
These represent *requests* to a specific server to give us a specific resource or *response*.

URLs contain a lot of information, so it is useful to understand the parts of an address.
Taking a careful look at a URL can help you evaluate a web page to better understand the source or judge the risk of a click.

To view the current URL in your browser, click in the address bar at the top of the window. 
To view the full URL in a hyperlink, hover your cursor over the link and look for URL to display in the lower left.

## Uniform Resource Locators

Let's dissect a URL:

{% include alert.html text="`https://example.com/about?key=value#anchor`" align="center" color="success" %}

protocol `://` domain `.` top-level domain `/` path and filename `?` query with parameters `#` anchor

<table class="table table-bordered table-striped mb-5">
    <tbody>
        <tr>
            <td><strong>Protocol</strong></td>
            <td>there is actually more than 100 defined Internet Protocols, however with URLs the most common is <a href="https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol">Hypertext Transfer Protocol (HTTP)</a>. "http://" is insecure, "https://" is secure and should be standard for all sites.</td>
        </tr>
        <tr>
            <td><strong>Domain</strong></td>
            <td>the <a href="https://en.wikipedia.org/wiki/Domain_Name_System">Domain Name System (DNS)</a> is often described as a "phone book" that translates easy to understand web addresses into the appropriate <a href="https://en.wikipedia.org/wiki/IP_address">IP addresses</a> of servers with the desired information. Domains end with a <code>.</code> and "top-level domain", e.g. ".com" or ".edu".</td>
        </tr>
        <tr>
            <td><strong>Subdomain</strong></td>
            <td>(optional) can be added in front of the main domain. For example, in "lib.uidaho.edu" > <code>lib</code> is a subdomain of <code>uidaho</code>, which is a subdomain of the top-level domain <code>edu</code>.</td>
        </tr>
        <tr>
            <td><strong>Port</strong></td>
            <td>(optional) occasionally added at the end of the domain, referring to specific communication endpoints that the server is listening on. For the web the standard ports are <code>:80</code> (http) and <code>:443</code> (https). This is rarely seen any more!</td>
        </tr>
        <tr>
            <td><strong>Path + filename</strong></td>
            <td>these can be imagined like folders and files on the server (and actually are in static web sites). For example, <code>/about/index.html</code>, is the index file in the "about" folder. If no filename is given, by default the server provides the file named <code>index</code>.</td>
        </tr>
        <tr>
            <td><strong>Query string</strong></td>
            <td>(optional) added to the end of an URL following a <code>?</code> and is given in key value pairs like <code>key=value</code>. Multiple pairs can be separated by <code>&</code>. The characters must be URL encoded / escaped, since some characters such as space are not allowed in URLs. The queries are processed by the server or javascript, so what exactly they do depends on the page. For example, <code>/index.php?title=example&action=edit</code> might return a wiki article in edit mode from a server running PHP.</td>
        </tr>
        <tr>
            <td><strong>Anchor</strong></td>
            <td>(optional) added to the end of a URL following a <code>#</code>. They traditionally correspond to specific element <code>id</code> on an HTML page, but are often used by javascript to add other functionality. For example, <code>/index.html#Chapter1</code> might jump to a chapter heading in the web page, or <code>/about.html#help</code> might pop up a modal.</td>
        </tr>
    </tbody>
</table>

## Static and Dynamic Web

Traditionally, web servers acted more or less like a read-only shared folder of files. 
The parts of a URL were basically just the paths to find documents in a folder.
So you can think of a website as a folder of files.

A <span class="term">static website</span> is just that--a collection of HTML, CSS, JS, images, and other files that are delivered exactly as they are on the server to users. 
A URL in a static site generally represents a request for an HTML document in a specific file location.
Static sites are simple and high performance.

In contrast a <span class="term">dynamic website</span> uses a server-side programming language to create pages on the fly when a user makes a request. 
Thus a URL represents a query, rather than an existing document on the server. 
Think of complex sites such as social media, where users are constantly adding more data and there is no "static" documents, but streams of every changing content.
None-the-less, what the server ultimately delivers to your browser is still HTML, CSS, and JS.

In these platforms content, templates, and metadata are usually stored in a database. 
For example, the popular [content management systems](https://en.wikipedia.org/wiki/Content_management_system) [WordPress](https://wordpress.com/) and [Drupal](https://www.drupal.org/) use the scripting language PHP and database MySQL.
This enables complex interactivity such as comments, customized views, user management, and a web-based admin interface.
