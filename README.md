# news_movies

Public host for **news videos posted to X**. Collect in [githito.xapi](https://github.com/Githitosh/githito.xapi) publishes stock JSON (and later media) here.

- **URL on video:** the X post 引用 URL is burned **inside the video picture at the bottom** of every frame / MP4 export (movies path only).
- **Data player** (settings + clickable URL links): [news_data](https://github.com/Githitosh/news_data) — separate repo.
- Stay **public** so X can reach the files. Do not privatize with the program/data repos.

## Live paths

| What | URL |
| --- | --- |
| Pages (after enable) | https://githitosh.github.io/news_movies/ |
| Stock (raw) | https://raw.githubusercontent.com/Githitosh/news_movies/main/v1/stock-news-ja.json |
| Stock EN | https://raw.githubusercontent.com/Githitosh/news_movies/main/v1/stock-news-en.json |

## Owner: enable GitHub Pages

1. Repo **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / folder `/` (root)
4. Save. Site appears at the Pages URL above.

Collect needs secret **`MOVIES_TOKEN`** on `githito.xapi` (fine-grained PAT: Contents read/write on `news_movies` and `reply_movies`). See the Project doc `docs/repo-split-movies-publish.md`.

## Layout

```
v1/stock-news-ja.json   # from Collect
v1/stock-news-en.json
index.html              # minimal X export player (URL burned on frames)
src/engine.js
lib/mp4-muxer.js
assets/bg_*.jpg
```
