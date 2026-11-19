# The Ask Yi I Ching

A complete English translation of the I Ching (Zhouyi, 周易) with the Chinese text beside it: all 64 hexagrams, 64 judgments, 384 line texts, and the two extra texts for hexagrams 1 and 2. 450 passages in total.

Translated by manpo for [Ask Yi](https://askyi.app). Free to use, including commercially, under CC BY 4.0. Short form of the name: "the Ask Yi translation".

Edition 2, version 2.0.0 · DOI: [10.5281/zenodo.24358845](https://doi.org/10.5281/zenodo.24358845)

## Where to find it

- Read online or download the PDF: https://askyi.app/i-ching-pdf/
- GitHub: https://github.com/manpoai/ask-yi-i-ching
- Hugging Face: https://huggingface.co/datasets/manpoai/ask-yi-i-ching
- Zenodo (DOI): https://doi.org/10.5281/zenodo.24358845
- Kaggle: https://www.kaggle.com/datasets/manpoai/ask-yi-i-ching
- Internet Archive (PDF): https://archive.org/details/ask-yi-i-ching-edition-2

## What is in it

| File | Contents |
| --- | --- |
| `data/iching.json` | Everything in one file: 64 hexagrams, each with its judgment and lines |
| `data/hexagrams.csv` | One row per hexagram, with the judgment |
| `data/lines.csv` | One row per passage, 450 rows |

Each hexagram has:

- `number`: King Wen order, 1 to 64
- `symbol`: the Unicode hexagram character
- `name`, `name_zh`, `pinyin`
- `binary`: the six lines from bottom to top, `1` for a solid (yang) line and `0` for a broken (yin) line
- `lower_trigram`, `upper_trigram`
- `judgment_zh`, `judgment`
- `lines`: six entries, each with `position` (1 is the bottom line, 6 is the top), `yang`, `label`, `label_zh`, `text_zh`, `text`
- `all_lines`: only on hexagrams 1 and 2, the text for when all six lines change

In `lines.csv`, `position` 0 is the judgment, 1 to 6 are the lines, and 7 is the all-lines text.

A sample:

```json
{
  "position": 1,
  "yang": true,
  "label": "Nine at the beginning",
  "label_zh": "初九",
  "text_zh": "潜龙勿用。",
  "text": "Hidden dragon. Do not act."
}
```

This version covers the core text only. The Ten Wings (the Image, the Commentary on the Judgment, and the other appendices) are not included.

## How it was translated

**The Chinese text** is the received text of the Zhouyi in simplified characters with modern punctuation.

**The readings** mainly follow Huang Shouqi and Zhang Shanwen, *Zhouyi Yizhu* (黄寿祺、张善文《周易译注》), a standard modern Chinese commentary. Where a word in the original can be read more than one way, the English takes the reading that fits that passage.

**The English translates the original text, not the commentary.** The original is terse and built from images: a dragon in a field, a fox crossing a river, a well with no lid. The translation keeps those images and keeps the sentences short. It does not add explanations in brackets or fold a commentator's advice into the line.

**The same word is not always the same English.** A word is translated the same way wherever it means the same thing, and differently where it means something different. The clearest case is 贞 (zhēn). In some passages it means the divination itself, and is translated that way: "The divination is auspicious." In others it means holding firm to what is right, and is translated "steadfast". Both readings have a long history, and this translation chooses between them passage by passage.

**Hexagram names** are the English names most readers already know, so that "Hexagram 11, Peace" here is the same hexagram a reader meets elsewhere.

## License and attribution

[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You can copy, adapt and build on this translation for any purpose, including commercial products, as long as you give credit.

Credit it like this, with the link:

> The Ask Yi I Ching, translated by manpo. https://askyi.app

In an app or a web page, a line such as "I Ching text: the Ask Yi translation by manpo (askyi.app)" is enough. If you changed the text, say so.

To cite it:

> manpo. *The Ask Yi I Ching*. Edition 2. Ask Yi, 2026. https://doi.org/10.5281/zenodo.24358845

## Corrections

If you find a mistake in the Chinese text or the translation, open an issue with the hexagram number and line. Corrections go into the next version, and each version is listed here.

- 2.0.0 (Edition 2): the whole translation revised passage by passage against the Chinese text; first release as open data under CC BY 4.0
- Edition 1: the first PDF edition, published on askyi.app under CC BY-NC 4.0
