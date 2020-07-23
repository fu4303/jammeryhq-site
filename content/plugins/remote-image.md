---
title: Remote Image
slug: remote-image
date: 2020-05-20
excerpt: Simple plugin to download remote images in Gridsome.
thumb: ./images/remote-image.jpg
image: ./images/remote-image-large.jpg
demo: https://remote-image.jammeryhq.com
repo: gridsome-plugin-remote-image
availability: 1
searchTerms: plugin, remote-image, performance
published: true
featured: false
guide: remote-image-plugin
---
This is a simple plugin, which is based on a discord discussion.
It's more a workaround than a permanent solution.

The plugin should work with any data source, but I have tested it only with `source-filesystem`.

## Features

* Download of remote images
* Support of multiple images ( see example )

## Install

```sh
npm i @noxify/gridsome-plugin-remote-image

# or

yarn add @noxify/gridsome-plugin-remote-image
```

## Setup

```js
//gridsome.config.js

module.exports = {
  siteName: 'Gridsome',
  plugins: [
    //...
    {
      use: '@noxify/gridsome-plugin-remote-image',
      options: {
        'typeName' : 'Entry',
        'sourceField': 'remoteImage',
        'targetField': 'imageDownloaded',
        'targetPath': './src/assets/remoteImages'
      }
    },
    {
      use: '@noxify/gridsome-plugin-remote-image',
      options: {
        'typeName' : 'Entry',
        'sourceField': 'remoteImages',
        'targetField': 'imagesDownloaded',
        'targetPath': './src/assets/remoteImages'
      }
    }
  ]
  //...
}
```

## Documentation

You can find the complete documentation here: https://webstone.info/documentation/gridsome-plugin-remote-image