# Jimce Deezer API Client

Ein TypeScript-basierter Deezer API Client für Node.js.

## Installation

```bash
npm install jimce-deezer-api
```

## Verwendung

### Grundlegende Nutzung

```typescript
import { DeezerClient } from 'jimce-deezer-api';

const client = new DeezerClient();

// Suche nach einem Track
const results = await client.search('Bella Napoli');
console.log(results);
```

### API Methoden

#### Suche
```typescript
// Nach hinten wird der vollständige SearchResult mit allen Track-Details zurückgegeben
const results = await client.search('Bella Napoli');
```

#### Tracks
```typescript
const track = await client.getTrack(<TRACK_ID>);
```

#### Alben
```typescript
const album = await client.getAlbum(<ALBUM_ID>);
```

#### Künstler
```typescript
const artist = await client.getArtist(<ARTIST_ID>);
```

#### Playlists
```typescript
const playlist = await client.getPlaylist(<PLAYLIST_ID>);
```

#### Podcasts
```typescript
const podcast = await client.getPodcast(<PODCAST_ID>);
```

#### Episodes
```typescript
const episode = await client.getEpisode(<EPISODE_ID>);
```

#### Radio
```typescript
const radio = await client.getRadio(<RADIO_ID>);
```

#### Chart (Top Charts)
```typescript
const chart = await client.getChart();
```

#### Genres
```typescript
const genres = await client.getGenres();
```

#### Editorial
```typescript
const editorial = await client.getEditorial();
```

#### API Informationen
```typescript
const infos = await client.getInfos();
const options = await client.getOptions();
```

## Typen

Das Package kommt mit vollständiger TypeScript-Unterstützung:

```typescript
import { Track, Album, Artist, SearchResult } from 'jimce-deezer-api';

const results: SearchResult = await client.search('Query');
const track: Track = results.data[0];
```

## Entwicklung

### Build
```bash
npm run build
```

### Watch Mode
```bash
npm run dev
```

## Lizenz

MIT
