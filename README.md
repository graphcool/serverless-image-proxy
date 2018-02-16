# serverless-image-proxy [![Build Status](https://travis-ci.org/graphcool/serverless-image-proxy.svg?branch=master)](https://travis-ci.org/graphcool/serverless-image-proxy) [![Greenkeeper badge](https://badges.greenkeeper.io/graphcool/serverless-image-proxy.svg)](https://greenkeeper.io/)
Resizes images using a Lambda function (aka Serverless Thumbor)

> Note: For this to work in a browser you have to add `*/*` to binary Media Types in API Gateway console.

## Notes

* Images are cropped before they are resized
* Cropping starts from left-top corner


## Syntax

> URL: `DOMAIN` **/** `VERSION` **/** `PROJECT_ID` **/** `FILE_SECRET` **/** [ `CROP` **/** ] `RESIZE` [  **/** `NAME` ]

### Resize

> Format: [ `X` ] **x** [ `Y` ]

* `500x300`: Fit into 500px x 300px rectangle
* `500x300!`: Forced resize
* `500x`: Resize to 500px width maintaining aspect ratio
* `x300`: Resize to 300px height maintaining aspect ratio
	
### Crop

> Format: `X` **x** `Y` **:** `WIDTH` **x** `HEIGHT`

* `0x0:400x400`: Crops the image taking the first 400x400 square

### Name

Name of image to improve indexing of images with search engines. 

Supported extensions: 

* png
* jpg
* jpeg
* svg
* gif
* bmp
* webp

## Development

Docker required to pre-build native NPM modules ([sharp](https://github.com/lovell/sharp)).

### Install

```sh
npm install --ignore-scripts
npm run prepare
serverless deploy
```

## Contributors

A big thank you to all contributors and supporters of this repository 💚

<a href="https://github.com/schickling/" target="_blank">
  <img src="https://github.com/schickling.png?size=64" width="64" height="64" alt="schickling">
</a>

<a href="https://github.com/huvik/" target="_blank">
  <img src="https://github.com/huvik.png?size=64" width="64" height="64" alt="huvik">
</a>

<a href="https://github.com/kbrandwijk/" target="_blank">
  <img src="https://github.com/kbrandwijk.png?size=64" width="64" height="64" alt="kbrandwijk">
</a>

## Help & Community [![Slack Status](https://slack.graph.cool/badge.svg)](https://slack.graph.cool)

Join our [Slack community](http://slack.graph.cool/) if you run into issues or have questions. We love talking to you!

![](http://i.imgur.com/5RHR6Ku.png)
