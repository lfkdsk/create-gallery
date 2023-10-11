# Create Gallery Intro

## 0. Folk this project [link](https://github.com/lfkdsk/create-gallery/fork)

## 1. Change Config

### Github Action

In `.github/workflows` :

``` yml
on:
  push:
    branches: [master]
  workflow_dispatch:
  # schedule:
  #   - cron: '0 12 * * *'

env:
  GIT_USER: lfkdsk # change to yourself
  GIT_EMAIL: lfkdsk@gmail.com # change to yourself
```

- Change `GIT_USER` and `GIT_EMAIL` with your own ones.
- Open `schedule` if you want to build daily. 

### Config.yml

```yml
# change to your own title, subtitle, cover... and author. 
title: Create Gallery Demo
subtitle: Take Photo Think Seriously
description: Create Gallery Demo 拿起相机，认真思考
cover: 'https://github.com/lfkdsk/picx-images-hosting/raw/master/20230817/IMG_7586.4e91my1ve140.17iz0sa56gik.webp'
author: lfkdsk

footer_logo: 
  use: self
  self:
    link: 'https://lfkdsk.github.io/'
    src: 'https://github.com/lfkdsk/picx-images-hosting/raw/master/20230817/tripper2white.2pbuwaqvndu0.webp'

# change to your url and sub url. eq: gallery 
url: https://lfkdsk.github.io/create-gallery
root: /create-gallery

# change to your slogan
photography_page:
  slogan: true
  slogan_descr: 'The moments when I pressed the shutter, the moments are forever.'

google_analytics: 
  use: gtag
  ga_id: 
  ga_api: 
  gtag_id: XXXXX

nav:
  归档: 
    link: https://lfkdsk.github.io # change to your links
    icon: inbox

thumbnail_url: https://cdn.jsdelivr.net/gh/lfkdsk/create-gallery@thumbnail/
base_url: https://cdn.jsdelivr.net/gh/lfkdsk/create-gallery@master
```

- `base_url` : `https://cdn.jsdelivr.net/gh/<github id>/<repo id>@master`
- `thumbnail_url`:  `https://cdn.jsdelivr.net/gh/<github id>/<repo id>@thumbnail/`

## 2. Add `GH_PAGES_DEPLOY`

1. Generate Github Token with repo permission:  https://github.com/settings/tokens/new

![](https://github.com/lfkdsk/picx-images-hosting/raw/master/repo/create-gallery/image-20231011153237388.4e0h8zozb5o0.webp)

2. Add it to repo's secrets as `GH_PAGES_DEPLOY`:

![](https://github.com/lfkdsk/picx-images-hosting/raw/master/repo/create-gallery/image-20231011152954709.1mmzihxlukdc.webp)

## 3. Add your new gallery page

1. Open PicX Tool & New Dir in root : 

![](https://github.com/lfkdsk/picx-images-hosting/raw/master/repo/create-gallery/image-20231011153413010.21ujm396c3gg.webp)

2. Select image and upload (recommand use webp and add watermark)

![](https://github.com/lfkdsk/picx-images-hosting/raw/master/repo/create-gallery/image-20231011153605385.3rn8nqccgo80.webp)

3. Add new config in `README.yml` 

```
Title:
  date: 2023-10-11
  url: Japan
  cover: Japan/XXXX.jpg

...
```


