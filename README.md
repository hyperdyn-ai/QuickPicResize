<!-- QuickPicResize API Documentation -->

<h1>QuickPicResize API Documentation</h1>

<!-- Introduction -->
<h2>Introduction</h2>
<p>QuickPicResize is a free API for dynamically resizing images to specific dimensions. This documentation provides details on how to use the API to resize images efficiently.</p>

<!-- API Endpoints -->
<h2>API Endpoints</h2>

<!-- Resize Image -->
<h3>Resize Image</h3>
<p>Endpoint: <code>POST /resize/api</code></p>

<!-- Parameters -->
<h4>Parameters:</h4>
<ul>
  <li><code>imageFile</code> (file): Image file to upload</li>
  <li><code>width</code> (integer): Desired width of the resized image</li>
  <li><code>height</code> (integer): Desired height of the resized image</li>
</ul>

<!-- Usage Examples -->
<h2>Usage Examples</h2>

<!-- Resize Image -->
<h3>Resize Image</h3>
<p>Resize an image with width 300px and height 200px.</p>

<!-- Command Line -->
<h4>Command Line:</h4>
<pre><code>curl -X POST -F "imageFile=@image.jpg" -F "width=300" -F "height=200" http://core.hyperdyn.cloud/resize/api</code></pre>

<!-- Response -->
<h4>Response:</h4>
<pre><code>{
  "status": "success",
  "message": "Image resized successfully",
  "resized_image_url": "http://core.hyperdyn.cloud/resized_image.jpg"
}
</code></pre>

<!-- Response Structure -->
<h2>Response Structure</h2>
<p>The API returns a JSON response with the following structure:</p>
<pre><code>{
  "status": "success" | "error",
  "message": "Description of the result",
  "resized_image_url": "URL of the resized image (if successful)"
}
</code></pre>
