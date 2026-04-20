# atexovi-ytmusic-api

<p align="center">
  <a href="https://www.npmjs.com/package/atexovi-ytmusic-api" target="_blank">
    <img src="https://img.shields.io/npm/v/atexovi-ytmusic-api?style=flat&logo=npm&logoColor=white&labelColor=CB3837&color=333" alt="npm version">
  </a>
  <a href="https://github.com/atex-ovi/ytmusic-api/blob/main/LICENSE" target="_blank">
    <img src="https://img.shields.io/npm/l/atexovi-ytmusic-api?style=flat&logo=opensourceinitiative&logoColor=white&labelColor=CB3837&color=333" alt="license">
  </a>
</p>

<p align="center">
  <a href="https://www.typescriptlang.org/">
    <img src="https://img.shields.io/badge/TypeScript-5.1-3178C6?style=flat&logo=typescript&logoColor=white" alt="TypeScript">
  </a>
  <a href="https://nodejs.org/">
    <img src="https://img.shields.io/badge/Node.js-16+-339933?style=flat&logo=nodedotjs&logoColor=white" alt="Node.js">
  </a>
  <a href="https://tsup.egoist.dev/" target="_blank">
    <img src="https://img.shields.io/badge/tsup-8.1.0-3178C6?style=flat&logo=typescript&logoColor=white" alt="tsup">
  </a>
  <a href="https://axios-http.com/" target="_blank">
    <img src="https://img.shields.io/badge/axios-1.7.2-5A29E4?style=flat&logo=axios&logoColor=white" alt="axios">
  </a>
  <a href="https://zod.dev/" target="_blank">
    <img src="https://img.shields.io/badge/zod-3.23.8-3068B7?style=flat&logo=zod&logoColor=white" alt="zod">
  </a>
</p>

---

> [!CAUTION]
> This package is **not official** YouTube Music API. It may break if YouTube changes their structure.

## Description

This is a fork of ytmusic-api with modifications for Node.js compatibility and Termux optimization.

*Live Demo: [ytmusic-player](https://ytmusic-player.vercel.app/)*

---

## For Package Users (npm)

Install from npm:

```bash
npm install atexovi-ytmusic-api
```

Then use:

```javascript
const YTMusicModule = require('atexovi-ytmusic-api');
const YTMusic = YTMusicModule.default;`

async function main() {`
    const ytmusic = new YTMusic();`
    await ytmusic.initialize();`
    const songs = await ytmusic.search("Never gonna give you up");`
    console.log(songs);`
}

`main();
```

---

## For Contributors (TypeScript Source)

> [!NOTE]
> This repository contains TypeScript source code.

### 1. Clone

```bash
git clone https://github.com/atex-ovi/ytmusic-api.git`
cd ytmusic-api
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Build

```bash
npm run build
```

Compiles TypeScript from `src/` to `dist/`

### 4. Run Tests

```bash
npm test
```

### 5. Lint

```bash
npm run lint
```

### 6. Clean

```bash
npm run clean
```

---

## Changes from Original

- Migrated from Bun to Node.js
- Removed bun-types dependencies
- Updated build configuration for Node.js
- Optimized for Termux and Android environments

---

## Features

- TypeScript Support
- Search Suggestions
- Songs
- Videos
- Artists
- Albums
- Playlists
- Lyrics
- Upcoming Songs

---

## API Methods

| Method | Description |
|--------|-------------|
| search(query) | Search for songs, videos, artists |
| getSearchSuggestions(query) | Get autocomplete suggestions |
| getArtist(artistId) | Get artist details and songs |
| getAlbum(albumId) | Get album tracks and info |
| getPlaylist(playlistId) | Get playlist songs |
| getLyrics(videoId) | Get song lyrics |
| getTrendingSongs() | Get trending music |

---


## Response Format

| Field | Type | Description |
|-------|------|-------------|
| videoId | string | YouTube video ID |
| name | string | Song title |
| artist | object | Artist information |
| artist.artistId | string or null | Artist unique ID |
| artist.name | string | Artist name |
| album | object | Album information |
| album.albumId | string | Album unique ID |
| album.name | string | Album name |
| duration | string or null | Song duration |
| thumbnails | array | List of thumbnail images |
| year | string or null | Release year |

---

## Tech Stack

| Technology | Version |
|------------|---------|
| TypeScript | 5.1 |
| Node.js | 16+ |
| tsup | 8.1.0 |
| axios | 1.7.2 |
| zod | 3.23.8 |

---

## Credits

| Role | Author | Package |
|------|--------|---------|
| Original Creator | Ateş Tan | [youtube-music-api](https://www.npmjs.com/package/youtube-music-api) |
| TypeScript Fork | zS1L3NT | [ytmusic-api](https://github.com/zS1L3NT/ts-npm-ytmusic-api) |
| Node.js Port | Atex Ovi | [atexovi-ytmusic-api](https://npmjs.com/package/atexovi-ytmusic-api) |

---

## License

[GPL-3.0](./LICENSE)

---
