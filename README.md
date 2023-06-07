
# Infinite Scroll JavaScript Project
This code represents an Infinite Scroll web application using the Unsplash API. It allows users to continuously load and display random photos from Unsplash as they scroll down the page. Here's a breakdown of the code:

### 1. HTML structure:

- The `<head>` section contains the necessary metadata, including the character encoding, viewport configuration, and page title.
- The external font and stylesheets are linked.
- The main HTML structure is defined within the `<body>` tag. It includes the title, loader, image container, and script.
### 2. CSS styles:

- CSS styles are embedded within the style.css file. They define the appearance and layout of various elements in the application.
- The font `"Bebas Neue"` is imported from Google Fonts.
- The styles define the layout of the title, loader, and image container.
- A media query is included to adjust the styles for smaller screens.
### 3. Title:

The application title is displayed using the `<h1>` tag.
### 4. Loader:

- The loader is represented by a `<div>` element with the class `"loader"` and the id `"loader"`. It is initially displayed while photos are being fetched, and hidden once the process is complete.
- An image is displayed within the loader to indicate the loading process.
### 5. Image Container:

- The image container is a `<div>` element with the class `"image-container"` and the id `"image-container"`. It is used to display the loaded images.
- Initially, it is empty, and images are dynamically added to it.
### 6. JavaScript functionality:

- The JavaScript code is enclosed within the <script> tags at the end of the HTML body.
- DOM elements are stored in variables using `document.getElementById`.
- Variables are initialized to track the loading state and the number of loaded and total images.
- The Unsplash API is used to fetch random photos. The count variable specifies the number of photos to fetch.
- The `imageLoaded` function is called whenever an image finishes loading. It keeps track of the number of loaded images and checks if all images have been loaded.
- The `setAttributes` function is a helper function used to set attributes on DOM elements.
- The `displayPhotos` function iterates over the fetched photos and creates HTML elements (`<a>` and `<img>`) for each photo. Event listeners are added to each image to track when it finishes loading.
- The `getPhotos` function is responsible for fetching photos from the Unsplash API. It makes an asynchronous request and then calls the displayPhotos function to render the fetched photos.
- The `window.addEventListener` listens for the scroll event. When the user scrolls near the bottom of the page and the ready flag is set, indicating that the previous set of photos has been loaded, it triggers the `getPhotos` function to fetch more photos.
- Finally, the `getPhotos` function is called to initiate the initial loading of photos.
