# WorldsApart language packs

One JSON pack per language for the WorldsApart SillyTavern extension, built by its `build-zipf.py` from [wordfreq](https://github.com/rspeer/wordfreq) by Robyn Speer. The data is [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/); wordfreq's sources include Google Books Ngrams, Wikipedia, OPUS OpenSubtitles 2018, ParaCrawl, the Leeds Internet Corpus and the SUBTLEX word lists by Marc Brysbaert et al., freely available data credited as wordfreq requires.

## What each language supports

| Language | Word frequency | Name detection | Parts of speech | Fragment detection | Segmenting |
| --- | --- | --- | --- | --- | --- |
| English (bundled with WorldsApart) | ✅ | ✅ capital letters | ✅ | ✅ | n/a |
| Español | ✅ | ✅ capital letters | ❌ | ❌ | n/a |
| Français | ✅ | ✅ capital letters | ❌ | ❌ | n/a |
| Polski | ✅ | ✅ capital letters | ❌ | ❌ | n/a |
| Português | ✅ | ✅ capital letters | ❌ | ❌ | n/a |
| Русский | ✅ | ✅ capital letters | ❌ | ❌ | n/a |
| Deutsch | ✅ | ❌ | ❌ | ❌ | n/a |

- **Word frequency**: how common each word is, plus a list of the most common words. Used by keyword suggestions and the Bulk Cleanup audit.
- **Name detection**: how WorldsApart finds names for relevance scoring. German capitalises every noun, so capital letters can't be used there.
- **Parts of speech**: keeps verbs and adjectives out of keyword suggestions.
- **Fragment detection**: flags a key that looks like a slice of a sentence.
- **Segmenting**: splitting text into words, for scripts written without spaces. None of the languages here needs it.

Each pack states the same in its `features` map, which is what WorldsApart reads.

`packs.json` is the index the extension reads; each language is `wa-pack-<lang>.json`. Adding a language is one build and a push.
