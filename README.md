#### Structure of an HTML Document

Every HTML page starts with a `<!DOCTYPE html>` declaration, followed by `<html>`, which is the root element. Inside `<html>`, there are two main sections:

* **Head section**: It contains meta-information about the document (like the title, links to stylesheets, and metadata).

* **Body section**: This is where the visible content (text, images, videos) goes.


Example:

```typescript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Basic HTML Page</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is a simple HTML document.</p>
</body>
</html>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727593937175/2f352474-6e47-4b9c-b3a9-703852fa336b.png)

---

#### Basic HTML Elements

* **Headings:** These elements (`<h1>` to `<h6>`) define headings. `<h1>` is the largest, and `<h6>` is the smallest.

    ```typescript
    <h1>Main Title</h1>
    <h2>Subheading</h2>
    ```


![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727596600395/78b8ffa9-a361-44e6-9d7c-61222a3ac2f6.png)

---

* **Paragraphs and Line Breaks:**

    * `<p>` defines a paragraph.

    * `<br>` is used for a line break.


    ```typescript
    <p>This is a paragraph of text.</p>
    <p>This is another paragraph.<br>With a line break inside.</p>
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727596625181/5c926ad9-c518-4b2f-a213-eca36450856a.png)
    
    ---

* **Links:** `<a href="URL">` is used to create hyperlinks.

    ```typescript
    <a href="https://www.example.com" target="_blank">Visit Example</a>
    ```

  ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727596667556/d3ad4ab6-49d8-435e-89dc-10237f679d9b.png)
    
  ---

* **Images:** The `<img>` element embeds an image.

    ```typescript
    <img src="image.jpg" alt="Description of the image" width="500">
    ```

  ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727596690114/52d4f31d-b5b9-4438-9406-8f1aecc98b6b.png)
    
  ---

* **Lists:**

    * **Ordered Lists (**`<ol>`): Numbered items.

        ```typescript
        <ol>
            <li>First item</li>
            <li>Second item</li>
        </ol>
        ```


    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727596800152/508d37f2-582b-4cb8-97e5-64a652def176.png)
    
    ---
    
    * **Unordered Lists (**`<ul>`): Bulleted items.
        
        ```typescript
        <ul>
            <li>Item one</li>
            <li>Item two</li>
        </ul>
        ```
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727596814878/6b3d7124-5fa2-4ddc-af1b-9e4cda8a554c.png)


---

#### Attributes

HTML attributes provide additional information about elements. Common attributes include:

* `href` for links, `src` for images, `alt` for images (describes the image for screen readers).

* `id` and `class` are used to assign unique or reusable identifiers to elements.


Example:

```typescript
<a href="https://example.com" class="link-button" id="learnMore">Learn More</a>
```

---

### **2\. Intermediate HTML**

#### Forms in HTML

Forms allow users to input data, which is sent to the server for processing. Key elements include:

* `<form>`: The container for all form elements.

* `<input>`: Used for various types of user input (text, password, email, checkbox).

* `<label>`: Associates text with a form element for accessibility.

* `<button>` and `<input type="submit">`: Submits the form.


Example:

```typescript
<form action="/submit" method="POST">
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" required>
    
    <label for="password">Password:</label>
    <input type="password" id="password" name="password">
    
    <input type="submit" value="Login">
</form>
```

#### Tables in HTML

Tables allow you to display data in rows and columns using the following elements:

* `<table>`: The container for the table.

* `<tr>`: Defines a row in the table.

* `<th>`: Defines a header cell.

* `<td>`: Defines a standard cell.


Example:

```typescript
<table border="1">
    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>
    <tr>
        <td>John</td>
        <td>30</td>
    </tr>
    <tr>
        <td>Jane</td>
        <td>25</td>
    </tr>
</table>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727597005182/d94d2e72-d1a4-48ae-b911-eab4413cd477.png)

---

#### Semantic HTML

Semantic elements give meaning to your content. They make it easier for search engines and assistive technologies to understand your page. Key semantic tags include:

* `<article>`: Independent content such as a blog post.

* `<section>`: A section of content, such as chapters or thematic groups.

* `<nav>`: Navigation links.

* `<header>` and `<footer>`: Top and bottom content areas of a page.

* `<aside>`: Side content, such as a sidebar.


Example:

```typescript
<article>
    <header>
        <h2>Blog Post Title</h2>
        <p>Written by Author</p>
    </header>
    <p>This is the content of the blog post.</p>
    <footer>
        <p>Published on Date</p>
    </footer>
</article>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727596849920/5c1ab94b-7a92-469d-974a-2ac61a02f424.png)

---

### **3\. Advanced HTML**

#### HTML5 APIs

1. **Local Storage API:** Local storage allows storing data locally in the user's browser that persists even after closing the browser. It’s useful for saving user settings, preferences, or small pieces of data.

   Example:

    ```typescript
    <script>
        // Storing data
        localStorage.setItem("username", "JohnDoe");
    
        // Retrieving data
        let username = localStorage.getItem("username");
        console.log(username);
    </script>
    ```

2. **Canvas API:** The `<canvas>` element is used to draw graphics (like charts or game elements) on a web page.

   Example:

    ```typescript
    <canvas id="myCanvas" width="200" height="100"></canvas>
    
    <script>
        var canvas = document.getElementById('myCanvas');
        var ctx = canvas.getContext('2d');
        ctx.fillStyle = "blue";
        ctx.fillRect(20, 20, 150, 100);
    </script>
    ```

3. **Geolocation API:** This API allows web applications to get the user's geographic location (with their permission).

   Example:

    ```typescript
    <button onclick="getLocation()">Get My Location</button>
    <p id="location"></p>
    
    <script>
        function getLocation() {
            if (navigator.geolocation) {
                navigator.geolocation.getCurrentPosition(showPosition);
            } else {
                document.getElementById('location').innerHTML = "Geolocation is not supported by this browser.";
            }
        }
    
        function showPosition(position) {
            document.getElementById('location').innerHTML = "Latitude: " + position.coords.latitude +
            "<br>Longitude: " + position.coords.longitude;
        }
    </script>
    ```


#### Drag and Drop API

This allows elements to be draggable and dropped into different parts of a web page.

Example:

```typescript
<div id="drag1" draggable="true" ondragstart="drag(event)">Drag me!</div>
<div id="dropZone" ondrop="drop(event)" ondragover="allowDrop(event)" style="border:1px solid black; width:200px; height:100px;">
    Drop here
</div>

<script>
    function allowDrop(event) {
        event.preventDefault();
    }

    function drag(event) {
        event.dataTransfer.setData("text", event.target.id);
    }

    function drop(event) {
        event.preventDefault();
        var data = event.dataTransfer.getData("text");
        event.target.appendChild(document.getElementById(data));
    }
</script>
```

---

### **4\. HTML Best Practices**

#### Accessibility (a11y)

* Use descriptive **alt** text for images.

* Use proper **labels** for form elements for screen readers.

* Ensure a clear **focus state** for interactive elements (like links and buttons) for keyboard navigation.


Example:

```typescript
<label for="email">Email:</label>
<input type="email" id="email" name="email" aria-label="Email Address">
```

#### SEO (Search Engine Optimization)

* **Title and meta tags**: Ensure that each page has a unique title and meta description.

    ```typescript
    <title>My Website</title>
    <meta name="description" content="This is a description of my website.">
    ```

* **Heading hierarchy**: Use proper heading levels (`<h1>`, `<h2>`, etc.) to structure your content.


#### Performance Optimizations

* **Lazy loading images**: Load images only when they are about to enter the viewport.

    ```typescript
    <img src="image.jpg" alt="Example" loading="lazy">
    ```

* **Minify HTML**: Remove unnecessary characters (whitespace, comments) to reduce file size.

* **Async and defer for scripts**: Load JavaScript files without blocking the page rendering.

    ```typescript
    <script src="script.js" async></script>
    ```

  GitHub Repository:

* [https://github.com/thirdygayares/htmlstructure.git](https://github.com/thirdygayares/htmlstructure.git)