# phoneme
<img src="docs/img/badges.svg">

Spanish grapheme-to-phoneme conversion in Go for webtyp's text-to-speech: written Spanish in,
IPA phonemes out, with the same symbols the Piper/Kokoro voices were trained on. It is MIT
licensed and has no espeak-ng dependency, which is GPL-3.

> **STATUS (remove this note when the first plan lands):** documentation only. Voice is
> version 2 of the agent.

## Why it exists

Speech models do not read letters. They read **phonemes**, the sounds of the language. The
usual converter, espeak-ng, is GPL-3, and putting it in the same binary as MIT libraries would
put the whole binary under GPL terms. Spanish spelling maps to sound with few, regular rules
(for example `c` before `e`/`i`, `qu`, `ll`, `rr`, stress by accent and word ending), so a
rule-based converter in Go is small, fast, and keeps the stack pure Go.
