<p align="center">
  <a href="https://soundboardio.com/app/developers/?utm_source=github&utm_medium=readme&utm_campaign=developers">
    <img src="icons/og-v2.jpg" width="640" alt="Developer's Pain">
  </a>
</p>

# Developer's Pain

> Plugin for [SoundBoardio.com](https://soundboardio.com), a free GitHub-powered soundboard app. This repository is also the template for your own board.

## Creating Sound Board

1. Create new repository on your Github, based on this repository.
   - Make sure your repository is **public** and its name starts with `soundboardio-`
   - Prepare your **sounds** (Github or self-hosted files)
   - Create your **[`soundboardio.json`](https://github.com/soundboardio/soundboardio-developers/blob/master/soundboardio.json) manifest**. Be creative. Choose name, description, colors and tiles, ... The [generator](https://soundboardio.com/generator/) builds it for you and the [validator](https://soundboardio.com/validator/) checks it.
   - Prepare **icons** (you will need at least two icons if you want your app to be installable). [See this example](https://github.com/soundboardio/soundboardio-developers/blob/master/soundboardio.json#L19)
2. Now you can just open your shiny new app with your own url. It's working automagically.

> If your repository is called https://github.com/ `soundboardio/soundboardio-developers` your SoundBoardio url will be https://soundboardio.com/ `app/soundboardio/developers`

The step-by-step guide lives at [soundboardio.com/create](https://soundboardio.com/create/).

## Lyrics (transcript)

A board can carry the transcript of its source video in `lyrics`. The page shows it under the tiles, and a tile with a `transcript` becomes playable right from the text.

```json
"lyrics": [
  "– Is it plugged in?",
  "– Yes. Have you tried turning it off and on again?"
],
"tiles": [
  { "name": "Off and on", "filename": "off-and-on.mp3", "transcript": "Have you tried turning it off and on again?" }
]
```

- One array item is one paragraph, or one speaker's turn when people talk. Plain text only, no `<br />` or other HTML: the text is also served as Markdown and structured data as it is.
- When more than one person speaks, every item starts with an en dash and a space (`– `), the narrator included. A monologue has no dashes.
- Every item ends with punctuation (`.`, `!`, `?`, `…`). Quotes inside use the language's own marks („…“).
- A tile's `transcript` is the quote exactly as it is worded inside a single lyrics item. Use it when the tile `name` is a looser label; the match is literal.

## Donation ❤️

This project and platform [SoundBoardio.com](https://soundboardio.com) is completely free and we're making it with love :)

If you want to help us, please consider [making a donation](https://soundboardio.com/donate/?utm_source=github&utm_medium=readme&utm_campaign=developers) for some 🍺 or 🍵 ;)

## License

Copyright &copy; 2026 [AquaSoup](http://aquasoup.com)

Proudly powered by nature 🗻, wind 💨, tea 🍵 and beer 🍺 ;)

All contents are licensed under the [MIT license].

[mit license]: LICENSE
