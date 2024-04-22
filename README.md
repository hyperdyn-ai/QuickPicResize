<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QuickPicResize API Documentation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 0;
            line-height: 1.6;
        }
        h1, h2, h3 {
            margin-top: 30px;
        }
        code {
            font-family: Consolas, monospace;
            background-color: #f4f4f4;
            padding: 5px;
            border-radius: 3px;
        }
    </style>
</head>
<body>
    <h1>QuickPicResize API Documentation</h1>

    <h2>Introduction</h2>
    <p>QuickPicResize is a free API for dynamically resizing images to specific dimensions. This documentation provides details on how to use the API to resize images efficiently.</p>

    <h2>API Endpoints</h2>

    <h3>Resize Image</h3>
    <p>Endpoint to resize an image to specified dimensions.</p>
    <pre><code>
POST /resize/api

Parameters:
- imageFile (file): Image file to upload
- width (integer): Desired width of the resized image
- height (integer): Desired height of the resized image
    </code></pre>

    <h2>Usage Examples</h2>

    <h3>Resize Image</h3>
    <p>Resize an image with width 300px and height 200px.</p>
    <pre><code>
curl -X POST \\
  -F "imageFile=@image.jpg" \\
  -F "width=300" \\
  -F "height=200" \\
  http://core.hyperdyn.cloud/resize/api
    </code></pre>

    <p>Response:</p>
    <pre><code>
{
  "status": "success",
  "message": "Image resized successfully",
  "resized_image_url": "http://core.hyperdyn.cloud/resized_image.jpg"
}
    </code></pre>

    <h2>Response</h2>
    <p>The API returns a JSON response with the following structure:</p>
    <pre><code>
{
  "status": "success" | "error",
  "message": "Description of the result",
  "resized_image_url": "URL of the resized image (if successful)"
}
    </code></pre>

</body>
</html>
