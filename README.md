# Image Hosting Module
Host images from your Mendix application!
 
# Configuration:
1. Add the InitializeImageHosting sub microflow to the after start up flow.
2. Add the overview snippet to a page and then add the page to your navigation 
3. Upload images to your database


# Usage:
When an image is uploaded to the image entity, there will be an attribute for the url to access the uploaded image.

This url can be used to embed images into emails using the html image tag


# Example:

```html
<img src="http://localhost:8080/image?Name=07CAT-STRIPES-mediumSquareAt3X-v2.jpg" width="500" height="600">
```



# Optional Setup: 
The request handler name and attribute to query on can be changed by updating the two constants in this module. 

The HostImage java action can be added to the after start up microflow for more advanced setup.

# Mx8
A Mendix 8 module can be found in github

# Disclaimer: 
This java action does not apply any database access rules to access the image, the main intent is to host images for anonymous users and allow the image to be embedded into emails. It is not recommended to configure the request handler to expose any entities from the system module or any entities that contain sensitive information. 