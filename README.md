# atexovi-ytmusic-api

<p align="center">
  <a href="https://www.npmjs.com/package/atexovi-ytmusic-api" target="_blank">
    <img src="https://img.shields.io/npm/v/atexovi-ytmusic-api?style=flat&logo=npm&logoColor=white&labelColor=CB3837&color=333" alt="npm version">
  </a>
  <a href="https://www.npmjs.com/package/atexovi-ytmusic-api" target="_blank">
    <img src="https://img.shields.io/npm/dt/atexovi-ytmusic-api?style=flat&logo=npm&logoColor=white&labelColor=CB3837&color=333" alt="npm total downloads">
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
  <a href="https://github.com/atex-ovi">
    <img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white" alt="GitHub">
  </a>
</p>

---

**atexovi-ytmusic-api** - YouTube Music API (Unofficial)  
Modified and maintained by [Atex Ovi](https://github.com/atexovi)

Original by [zS1L3NT](https://github.com/zS1L3NT/ts-npm-ytmusic-api)

## Description

This is a fork of ytmusic-api with modifications for Node.js compatibility and Termux optimization. Original package by [zS1L3NT](https://github.com/zS1L3NT/ts-npm-ytmusic-api).

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

## Installation

```bash
npm install atexovi-ytmusic-api
```
---

## Usage

### CommonJS (Node.js)

```javascript
const YTMusicModule = require('atexovi-ytmusic-api');
const YTMusic = YTMusicModule.default;

async function main() {
    const ytmusic = new YTMusic();
    await ytmusic.initialize();
    
    const songs = await ytmusic.search("Never gonna give you up");
    console.log(songs);
}

main();
```

### ES Modules

```javascript
import YTMusic from 'atexovi-ytmusic-api';

const ytmusic = new YTMusic();
await ytmusic.initialize();

const songs = await ytmusic.search("Never gonna give you up");
console.log(songs);
```

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

| Role | Contributor |
|------|-------------|
| Original Author | [zS1L3NT](https://github.com/zS1L3NT/ts-npm-ytmusic-api) |
| Modified by | [Atex Ovi](https://github.com/atex-ovi) |

---

## License

[GPL-3.0](./LICENSE)

---
