```markdown
# QuickPicResize API Documentation

## Introduction
QuickPicResize is a free API for dynamically resizing images to specific dimensions. This documentation provides details on how to use the API to resize images efficiently.

## API Endpoints

### Resize Image
Endpoint: `POST /resize/api`

**Parameters:**
- `imageFile` (file): Image file to upload
- `width` (integer): Desired width of the resized image
- `height` (integer): Desired height of the resized image

## Usage Examples

### Resize Image
Resize an image with width 300px and height 200px.

**Command Line:**
\```bash
curl -X POST -F "imageFile=@image.jpg" -F "width=300" -F "height=200" http://core.hyperdyn.cloud/resize/api
\```

**Response:**
\```json
{
  "status": "success",
  "message": "Image resized successfully",
  "resized_image_url": "http://core.hyperdyn.cloud/resized_image.jpg"
}
\```

## Response Structure
The API returns a JSON response with the following structure:

\```json
{
  "status": "success" | "error",
  "message": "Description of the result",
  "resized_image_url": "URL of the resized image (if successful)"
}
\```
```
