# PictShare version 2
---
[![Apache License](https://img.shields.io/badge/license-Apache-blue.svg?style=flat)](https://github.com/HaschekSolutions/pictshare/blob/master/LICENSE)

# This is the development branch for Version 2 do not use in production
Test site: https://dev.pictshare.net/ (only sometimes on)

Table of contents
=================
* [Installation](/rtfm/INSTALL.md)
* [Docker](/rtfm/DOCKER.md)
* [API](/rtfm/API.md)
* [Addons/Integration](/rtfm/INTEGRATIONS.md)

---

## New Features in v2:

- Added text hosting (like pastebin)
- Added URL shortening
- Added WebP to images (and conversion from jpg,png to webp)
- Massive code rework. Actually we designed it from the ground up to be more modular and easier to debug

## Breaking changes

- [New API system](/rtfm/API.md). Only single file uploads now via /api/upload.php (POST var name is "file"). [read more..](/rtfm/API.md)
- Data directory renamed from ```upload``` to ```data```
- Backblaze support dropped for now because we didn't need it anymore as ALT_FOLDER is more flexible. If soneone needs it, it can easily be implemented via adding a new storage controller. We're happy to accept pull requests

## Status

- [x] Duplicate detection
- [x] Write permission detection
- [x] Delete codes for every uploaded file
- [x] Upload via link/url
- [x] Upload via base64
- [ ] Autodestruct for every uploaded file

### Config options

Read [here](/rtfm/CONFIG.md) what those options do

- [x] ALT_FOLDER
- [x] URL (instead of FORCE_DOMAIN but mandatory)
- [x] LOG_UPLOADER
- [x] FFMPEG_BINARY
- [x] PNG_COMPRESSION
- [x] JPEG_COMPRESSION
- [x] WEBP_COMPRESSION
- [x] MASTER_DELETE_CODE
- [x] MASTER_DELETE_IP
- [x] UPLOAD_FORM_LOCATION
- [ ] UPLOAD_QUOTA
- [ ] UPLOAD_CODE
- [ ] LOW_PROFILE
- [ ] IMAGE_CHANGE_CODE
- [ ] MAX_RESIZED_IMAGES
- [ ] ALLOW_BLOATING
- [ ] BACKBLAZE

### Image hosting
- [X] Resizing
- [ ] Filters
- [x] Gif to mp4 conversion
- [x] Upload of images

### Text file hosting
- [x] Upload of text files
- [x] Render template for text files
- [x] Raw data view
- [x] Downloadable

### URL shortening
- [ ] Upload of links to shorten

### MP4 hosting
- [x] Resizing
- [x] Preview image generation
- [x] Upload of videos
- [x] Automatic conversion if not mobile friendly or wrong encoder used
- [x] Render template for videos


---

This is a [HASCHEK SOLUTIONS](https://haschek.solutions) project

[![HS logo](https://pictshare.net/css/imgs/hs_logo.png)](https://haschek.solutions)