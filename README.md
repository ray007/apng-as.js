# apng-as.js
A small, fast and advanced APNG assembler. It started as a fork of [UPNG.js](https://github.com/photopea/UPNG.js), but can now only assemble multiple single-image png frames to one apng image.

I'm using it to diplay animations in the browser, it's the opposite of [apng-canvas](https://github.com/davidmz/apng-canvas).

## Encoder

UPNG.js supports APNG and the interface expects "frames". Regular PNG is just a single-frame animation (single-item array).

Other than the original UPNG.js, the input data consists of png image data instead of rgba data.

#### `UPNG.assemble(imgs, dels, [w, h])`
* `imgs`: array of frames. A frame is an ArrayBuffer containing the pixel data (RGBA, 8 bits per channel)
* `dels`: array of delays for each frame (only when 2 or more frames)
* `w`, `h` : width and height of the image, if not given taken from first frame
* returns an ArrayBuffer with binary data of a APNG file
