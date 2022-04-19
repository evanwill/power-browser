---
section: The Web
nav_order: 2
title: Addresses
---

understanding urls helpful for evaluating websites, information

# Uniform Resource Locators

Of course to get that code we need an web address. 
The links in your browser address bar are Uniform Resource Locators, **URLs**.

Let's dissect a URL:

{% include alert.md text="`https://example.com/about?key=value#anchor`" align="center" color="success" %}

protocol `://` domain `.` top-level domain `/` path and filename `?` query with parameters `#` anchor

<table class="table table-bordered table-striped">
    <tbody>
        <tr>
            <td><strong>Protocol</strong></td>
            <td>there is actually more than 100 defined Internet Protocols, however with URLs the most common is <a href="https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol">Hypertext Transfer Protocol (HTTP)</a>.</td>
        </tr>
        <tr>
            <td><strong>Domain</strong></td>
            <td>the <a href="https://en.wikipedia.org/wiki/Domain_Name_System">Domain Name System (DNS)</a> is often described as a "phone book" that translates easy to understand web addresses into the appropriate <a href="https://en.wikipedia.org/wiki/IP_address">IP addresses</a> of servers with the desired information.</td>
        </tr>
        <tr>
            <td><strong>Subdomain</strong></td>
            <td>(optional) can be added in front of the main domain. For example, in "lib.uidaho.edu" > <code>lib</code> is a subdomain of <code>uidaho</code>, which is a subdomain of the top-level domain <code>edu</code>.</td>
        </tr>
        <tr>
            <td><strong>Port</strong></td>
            <td>(optional) occasionally added at the end of the domain, referring to specific communication endpoints that the server is listening on. For the web the standard ports are <code>:80</code> (http) and <code>:443</code> (https).</td>
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
