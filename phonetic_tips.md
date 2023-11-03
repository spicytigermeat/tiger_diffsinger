# Phonetic Editing Tips 🔤
By default, you will get good results with Tiger using the `DIFFS EN X` phonemizer. This phonemizer uses `dsdict-enx.yaml` and if a word is not listed in there, it will default to `ArpaXG2p`.
Below are some more specific tips that you may prefer over the default phonetics.
***
### Note Attack and Release
#### Attack ↗️
You can add `[vf]` to most samples to synthesize vocal fry. Please note that the pitch model may struggle to generate pitch for vocal fry as it's generally inconsistent.
Having the pitch curve slope down and move up with vocal fry will generally produce the best results. You can use `[vf]` at any point of a phonetic phrase, but best results
will be achieved when the majority of the `[vf]` is within a vowel.

If you feel that the attack of a note that is just a vowel is not snappy enough, adding `[q]` to the beginning will cause the note to begin with less of a fade in and more of
a snappyness. `[q]` may be used with a consonant as well, but results will vary in quality.

To achieve a breath before a sample, draw a new note, change the lyric to `-` and change the phoneme to `[AP]`. The `[AP]` is DiffSinger's default phoneme for 'Silence with a breath in it.' (not a quote)
#### Release ↘️
`[vf]` and `[q]` will do similar things in releases that they will do in attacks. `[vf]` can end a note with a vocal fry, and it's recommended to tune the pitch of the `[vf]` to be descending.
`[q]` will end a note snappier and quicker than normal, but may also sound like a `[t]` stop if it comes after a vowel.

To achieve a louder exhale, you can add `[hh]` to the end of a note.
***
### Accent Specifics
Tiger's accent is "American: Inland North" according to [Aschmann's map of American accents](https://aschmann.net/AmEng/). Generally, his accent is very neutral when compared to other American accents.
#### `[cl]`
Tiger's `[t]` tends to rest on the more relaxed side of the spectrum, meaning most single `[t]`'s, especially in the coda of a syllable tend to sound more like a `[tcl]`. 
(from the TIMIT extension of the Arpasing phonetic alphabet) To account for this, Tiger's `dsdict-enx.yaml` has many exceptions to include `[cl]` after words ending with `[t]`. `[cl]` can be used
to modify any plosive consonant, removing the 'pop' that follows. However, due to the nature of recording, you may find `[t]` at the end to also sound the same.
#### `[ch r]` vs `[t r]`
Ah, the age old question! In major commercial synthesizers, you may see that they include the phonemes `[tr]` and `[dr]` to represent the onset phoneme cluster in words like `tree` and `dress`. 
In Tiger's dataset, this is labelled as `[ch r]` and `[t r]` respectively, however either way will provide similar results, but using `[ch]` is recommended.
***
### Non-English Tips & Tricks
#### PT-BR
Brazilian Portuguese has nasal vowels, and while Tiger has data sang in PT-BR, the phonetic system in place does not allow for nasal vowels. A workaround that I've had success with is something like this:

`coração` - `[k oo dx aa s ax n w]` (the `[n]` would be edited in the phoneme timing editor in OpenUTAU to be as short as possible.)
