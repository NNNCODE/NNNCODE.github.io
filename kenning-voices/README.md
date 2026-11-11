# Kenning voices

Pronunciation files for [Kenning](https://chromewebstore.google.com/detail/khkapaoajbgmlnhobbmfekdlibkadaep),
a hover dictionary for people learning English. There is one file for each word in Kenning's
built-in dictionary — 58,226 words — and each was read once by
[Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) in the voice `af_heart`.

## The files

    af_heart-24k/<word>.opus

- Ogg Opus, 24 kHz, mono, 24 kbps. About 2.4 KB a word.
- The quiet before and after each word is trimmed to 40 ms and 80 ms.
- An apostrophe is written `_27`: `ain't` is `ain_27t.opus`. A hyphen stays as it is.
- Each file was decoded back by the browser that encoded it before it was kept.
  `af_heart-24k/render.json` records how the files were made.

## How Kenning uses them

When you press the speaker on a word card, Kenning first asks for that word's file here. If
there is none, or it does not play, Kenning plays the dictionary's recording, and then the
computer's own voice. Nothing is requested until you press the speaker.

GitHub Pages receives each request, so GitHub sees the word and your IP address, as with any
web request. See [Kenning's privacy policy](https://nnncode.github.io/lexi-hover/privacy.html)
and [GitHub's privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

Questions and problems: <https://github.com/NNNCODE/NNNCODE.github.io/issues>.

## Licence

The audio files are dedicated to the public domain under
[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/). You may use them for any
purpose without asking. Kokoro-82M, which read them, is licensed Apache-2.0.
