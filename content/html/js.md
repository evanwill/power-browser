---
section: HTML
nav_order: 4
title: JS
---

JavaScript is a programming language originally designed for interacting with HTML in the web browser
(note: it is *not* related to [Java](https://go.java/index.html)).
JS has evolved into a powerful, multipurpose language that enables advanced interactivity and data processing on the **client-side**, i.e. in your web browser rather than on the server.

Similar to CSS, JS can be written inline, in a script tag, or in an external file.

## Inline JS Attributes

Add an input button with the JS "onclick" attribute:

`<button type="button" onclick="document.getElementById('alert').innerHTML = 'Hello!'">Inline JS</button>`

Adding JS inline is simple, but has the same draw backs as inline CSS, mixing HTML semantic content with the visual presentation.

## Script Tag

JS contained in a `<script>` element will be executed in order as the HTML loads.
Unless they are critical to immediate presentation, scripts are often added towards the bottom of the HTML file to optimize load times.

Let's add another button:

`<button type="button" id="pop">Pop Up</button>`

Then attach a function using a script tag:

```
<script>
    /* set variables */
    var btn = document.getElementById('pop');
    var message = "Hello World!";
    /* create a function */
    function myAlert () {
        alert(message);
    }
    /* add event listener to element */
    btn.addEventListener("click", myAlert);
</script>
```

## External Files

As with CSS, JS will often be contained in a separate file that is loaded by the HTML document. 
Add a `src` attribute to a script tag to load JS:

`<script src="example.js"></script>`

Often, this will be external libraries that simplify adding advanced features to your site.
For example, Bootstrap bundle:

```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
```

Now, with Bootstrap CSS and JS bundle being loaded on our HTML file, try adding a [Modal](https://getbootstrap.com/docs/5.1/components/modal/):

```
<!-- Button trigger modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
  Click Me!
</button>

<!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">This is a Modal</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        A Bootstrap Modal!
      </div>
    </div>
  </div>
</div>

```

Notice that we didn't have to write any JS to add the Modal example. 
Bootstrap's library takes care of it all if you follow the mark up pattern (basically adding the `data-bs-target` attribute).

{% include alert.html text="To debug JS, be sure to open your browser's dev tools and look at the **Console**. Any error messages will appear there! You can also use `console.log()` to send debug messages from your script." color="success" %}
