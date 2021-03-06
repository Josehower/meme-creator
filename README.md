Overview:

This NPM module is for developers to create memes using an image URL, and save it into their specified directory.

Example meme:
![Meme](/memes/my_meme.jpeg)

Example code and usage:
**This module depends on the "jimp" NPM module**

```javascript
var memeCreator = require('meme-creator');
// var Jimp = require('jimp');

let options = {
    imageURL: 'https://puu.sh/FFRao/b67dde72b7.jpg', // URL to image
    topText: 'Daddy, what are clouds made of?', // top text of meme
    bottomText: 'Linux servers, mostly', // bottom text of meme
    directory: './memes/', // where to save memes
    fileName: 'my_meme', // change to 'random' for a random file name
}

memeCreator(options, function(res, error) {
    if(error) throw new Error(error)
    console.log('You can view your meme by going to ' + res.fileName);
});
```
