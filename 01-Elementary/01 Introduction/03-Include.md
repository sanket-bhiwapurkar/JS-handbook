# Questions

- 01 How/(In how many ways) can we include JS code in html? or:
- 02 Explain the `<script>` tag in detail.

# include

## The `<script>` Tag

In HTML, JavaScript code is inserted between `<script>` and `</script>` tags.

```HTML
<script>
document.getElementById("demo").innerHTML = "My First JavaScript";
</script>
```

### JavaScript in `<head>`

In this example, a JavaScript function is placed in the `<head>` section of an HTML page.

The function is invoked (called) when a button is clicked:

```HTML
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>
</head>
<body>

<h2>Demo JavaScript in Head</h2>

<p id="demo">A Paragraph</p>
<button type="button" onclick="myFunction()">Try it</button>

</body>
</html>
```

### JavaScript in `<body>`

In this example, a JavaScript function is placed in the `<body>` section of an HTML page.

The function is invoked (called) when a button is clicked:

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Demo JavaScript in Body</h2>

<p id="demo">A Paragraph</p>

<button type="button" onclick="myFunction()">Try it</button>

<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>

</body>
</html>
```

## External JavaScript

Scripts can also be placed in external files:

`myScript.js`

```JS
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
```

External scripts are practical when the same code is used in many different web pages.

JavaScript files have the file extension .js.

To use an external script, put the name of the script file in the src (source) attribute of a `<script>` tag:

```HTML
 <script src="myScript.js" type="text/javascript"></script>
```

### External JavaScript Advantages

Placing scripts in external files has some advantages:

- It separates HTML and code
- It makes HTML and JavaScript easier to read and maintain
- Cached JavaScript files can speed up page loads

### External References

An external script can be referenced in 3 different ways:

- With a full URL (a full web address) "https://www.w3schools.com/js/myScript.js"
- With a file path (like /js/) "/js/myScript.js"
- Without any path "myScript.js"
