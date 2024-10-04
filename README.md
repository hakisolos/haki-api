![Furina](https://i.imgur.com/mgvEIuY.jpg)

# HAKI-API

An API package providing various utilities, including media downloading and processing features.

## Installation

You can install `haki-api` using npm:

```bash
npm install haki-api
```

## HAKI API Features

- [Pinterest Downloader](#pinterest)
- [MediaFire Downloader](#mediafire)
- [Telegraph Uploader](#telegraph)
- [TikTok Downloader](#tiktok)
- [Uguu Uploader](#fileuguu)
- [M3U8 Converter](#m3u8)

## Pinterest <a name="pinterest"></a>

Download media from Pinterest.

```js
const { pinterest } = require('haki-api');
//import { pinterest } from 'hakian-api';

(async () => {
  console.log(await pinterest('https://in.pinterest.com/pin/617204323960160868/'));
})();
```
_You can use [pin.it](https://pin.it) and [in.pinterest.com](https://in.pinterest.com) URLs._

## MediaFire <a name="mediafire"></a>

Download files from MediaFire.

```js
const { mediafire } = require('haki-api');
//import { mediafire } from 'haki-api';

(async () => {
  console.log(await mediafire('https://www.mediafire.com/xyz.zip'));
})();
```

## Telegraph <a name="telegraph"></a>

Upload images to Telegraph.

```js
const { telegraph } = require('haki-api');
//import { telegraph } from 'haki-api';

(async () => {
  console.log(await telegraph('./img.png'));
})();
```

## TikTok <a name="tiktok"></a>

Download videos from TikTok.

```js
const { tiktok } = require('haki-api');
//import { tiktok } from 'haki-api';

(async () => {
  console.log(await tiktok('https://www.tiktok.com/videourl'));
})();
```

## File Uploader to Uguu <a name="fileuguu"></a>

Upload images to Uguu .

```js
const { fileUguu } = require(haki-api');
//import { fileUguu } from 'haki-api';

(async () => {
  console.log(await fileUguu('./img.png'));
})();
```

## M3U8 Converter <a name="m3u8"></a>

M3U8 to MP4

```js
const { m3u8 } = require('haki-api');
//import { m3u8 } from 'haki-api';

const convert = new m3u8();
convert.InputFile('https://file.m3u8') //also can be a path
             .OutputFile('./output.mp4') //default is output.mp4
             //.UseCLI(true); if you want to process it using CLI
             .start({
                onStart: () => console.log('Processing started...'),
                onEnd: () => console.log('Processing finished!')
             });
```
Complete `start` options

```js
.start({
    onStart: () => console.log('Processing started...'),
    onEnd: () => console.log('Processing finished!'),
    onProgress: (progress) => console.log(`Progress: ${progress}`),
    onStderr: (stderr) => console.error(`Error: ${stderr}`),
    onCodecData: (data) => console.log(`Codec Data: ${data}`),
    onError: (error) => console.error(`Error: ${error}`)
});
```
------

### Coming Soon

This package is under development, and many exciting features are planned for future releases. Stay tuned for updates and enhancements!

## Contributing

We welcome contributions! If you find any issues or have suggestions for improvement, feel free to open an issue or submit a pull request. If you want to contact me, check my [GitHub profile](https://github.com/hakisolos).

## CREDITS 
- HAKI
-IRON MAN
-GIFTED TECH

Copyright © 2024 HAKI & IRON-M4N
