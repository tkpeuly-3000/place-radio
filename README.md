# Place Radio 📻

**Type any city in the world. Its live weather picks the soundtrack, and real music plays nonstop like a radio.**

Rain in London plays sad songs. A windy afternoon in Lubbock plays restless, driving tracks. A clear night in Tokyo plays late night R&B. After every song, Place Radio checks the sky again, so when the weather changes, the music changes with it.

<p align="center">
  <img src="screenshots/phone.png" width="300" alt="Place Radio on a phone, tuned to a rainy day in London">
  &nbsp;&nbsp;
  <img src="screenshots/settings.png" width="300" alt="Station settings: music mode, languages, era slider and vibe picker">
</p>

## Try it

**Live app:** `https://YOUR-USERNAME.github.io/place-radio/`
(version without the spinning CD: `https://YOUR-USERNAME.github.io/place-radio/no-cd/`)

No sign in, no account, no API key. Open the link, press Play once, and it keeps going.

## How it works

1. **Find the city** with the Open Meteo geocoding API, picking the biggest matching city so "Paris" means Paris, France
2. **Scan the weather:** conditions, temperature, wind, humidity, local time and sunrise or sunset
3. **Pick a vibe** with a rule based algorithm that turns those readings into one of 23 moods
4. **Search for songs** that match the vibe, the chosen music mode, languages and era
5. **Play the video** in an embedded YouTube player, then rescan the sky and repeat

### The 23 weather vibes

| Group | Vibes |
|---|---|
| Sun | Sunshine heat, Golden day, Crisp & bright, Golden hour, Heatwave |
| Night | Starry night, After midnight, Cloudy night, Rainy night |
| Clouds & air | Grey sky mood, Foggy dream, Windy day, Sticky & humid, Desert dry |
| Rain & storms | Soft drizzle, Passing showers, Rainy day, Ice rain, Thunderstorm, Hailstorm |
| Snow & cold | Snow day, Blizzard, Deep freeze |

Each vibe has its own animated sky: rain, snow, blizzards, hail, lightning, fog, drifting clouds, stars, wind streaks with blowing leaves, desert dust, heat shimmer, icy sparkles and a low golden hour sun.

## Features

**Radio**
* Press Play once, then it plays song after song on its own
* Rescans the weather before every song and every Skip
* Never repeats a song until 30 others have played, and catches duplicate uploads of the same song
* Skips 10 hour mixes and anything that isn't a real song length
* Backup players and a backup song list keep the music going if a source fails

**Your station**
* **Music mode:** International hits, Top Billboard hits, or Local (music from the city's own country and language)
* **Languages:** any language, or up to 5 preferred ones, with suggestions while you type
* **Era:** Auto, a tuning dial slider from the 60s to the 2020s, or a specific year
* **Vibe:** follow the weather automatically, or pick your own from a category dropdown
* Setting changes wait for the next song instead of cutting off the one playing

**Controls and saved stuff**
* Play, Pause, Skip, Prev, a seek bar, volume and a sleep timer
* ♥ to like a song, ✕ to ban it forever
* Saved city stations, a Played history and a Liked list
* **Play liked:** shuffle only your liked songs, with no repeats until all have played
* Installs to a phone home screen like an app, with its own icon

<p align="center">
  <img src="screenshots/desktop.png" width="720" alt="Place Radio on a laptop">
</p>

## Built with

* Plain **HTML, CSS and JavaScript** in a single file, with no frameworks and no build step
* [Open Meteo](https://open-meteo.com/) for free weather and geocoding data
* The YouTube IFrame Player API for playback
* Public YouTube front ends (Piped and Invidious) to search songs without a sign in
* HTML Canvas for the weather animations
* A web app manifest and service worker so it installs like an app
* Browser localStorage for history, likes and settings (stays on your device)

## Run it yourself

Download this repo and open `index.html` in Chrome, Edge or Safari. For the smoothest YouTube playback, host it on a real web address, such as GitHub Pages.

## Notes

* Music plays through YouTube's own embedded player, so YouTube decides whether ads appear. Nothing is downloaded or ripped.
* Languages and eras steer the search words. Songs written in a different alphabet are filtered reliably; the ✕ button handles anything else that slips through.

## About

Made by **Tabassum Peuly**, a Mechanical Engineering student at Texas Tech University, as a personal project. Built with help from Claude as an AI coding partner.

## License

MIT, see [LICENSE](LICENSE).
