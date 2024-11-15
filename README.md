# Picture in Picture

This project is a Picture-in-Picture feature created as part of the course "JavaScript Web Projects: 20 Projects to Build Your Portfolio" by Zero To Mastery. It allows users to select a media stream from their screen and view it in a Picture-in-Picture mode.

## Table of contents

- [Picture in Picture](#picture-in-picture)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

This project enables users to:
- Select a screen or window to view in Picture-in-Picture mode.
- Click the "Start" button to initiate Picture-in-Picture for the selected media stream.

### Screenshot

![](./screenshot.png)

### Links

- Live Site URL: [DT Code](https://picture-in-picture.dtcode.se/)

## My process

### Built with

- HTML5 for structure
- CSS3 for styling
- JavaScript (ES6+) for functionality
- Web APIs (MediaDevices and Picture-in-Picture API)

### What I learned

In this project, I learned how to work with the Picture-in-Picture API and the MediaDevices API to allow users to select and view a media stream. I also gained experience handling async functions and incorporating media features in JavaScript.

Example code for selecting a media stream and enabling Picture-in-Picture:

```js
async function selectMediaStream() {
    try {
        const mediaStream = await navigator.mediaDevices.getDisplayMedia();
        videoElement.srcObject = mediaStream;
        videoElement.onloadedmetadata = () => {
            videoElement.play();
        }
    } catch (error) {
        console.log(error);
    }
}
```

### Useful resources

- [Picture-in-Picture API Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Picture-in-Picture_API) - Helped in understanding how to implement Picture-in-Picture functionality.
- [MediaDevices.getDisplayMedia()](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getDisplayMedia) - A helpful guide for setting up screen sharing.

## Author

- GitHub - [@dantvi](https://github.com/dantvi)
- LinkedIn - [@danieltving](https://www.linkedin.com/in/danieltving/)

## Acknowledgments

Special thanks to Zero To Mastery for providing the course and project guidance.
