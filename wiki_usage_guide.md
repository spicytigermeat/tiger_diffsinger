# :tiger: TIGER DS β :tiger:
Thanks for taking the time to read Tiger's usage guide! Below you will find some information to assist in using Tiger's DiffSinger models.

## 🌈 Installation 🌈
To install Tiger, simply drag and drop the ```TigerDS_b01.zip``` file into OpenUTAU. Accept the window that opens up. Then, ensure the hifi-gan vocoder released by [fish-diffusion](https://github.com/fishaudio/fish-diffusion/releases/tag/v2.0.0) is installed.
To install this, download ```fish-hifigan.oudep``` from this repo. and drag that file into OpenUTAU and accept the prompt. You are now ready to use Tiger!

## 🎵 OpenUTAU Usage 🎵
This voicebank is meant to be used in ```OpenUTAU```, and should be propely configured upon using for the first time. However, there are a few different options to choose from to change the way you use Tiger!
### 🔤 Supported Phonemizers 🔤
By default, Tiger will produce the best results with the ```DIFFS EN X``` phonemizer, which is a phonemizer I contributed to OPU that utilizes the ```[ax]``` and ```[dx]``` phonemes for more accurate American English. This phonemizer reads from ```dsdict-enx.yaml``` in the main folder, as well as in ```dsdur``` and ```dspitch```.
To overwrite the lyrics typed in each note, you can add ```[]``` after the lyrics and include phonemes between the brackets. For example: ```cut[k ax t]```.<br><br>
If you would like to do **phonetic only input** (bypass the ```[]``` requirement), you can use the basic ```DIFFS``` phonemizer. An added bonus to this mode is the ability to read a phoneme table for Japanese Hiragana from ```dsdict.yaml```.<br><br>
The ```DIFFS EN``` phonemizer is supported, but not by Tiger officially, and will simply use the estimated output from the ```ArpabetG2p```. (Not Recommended)<br>
### 📢 Custom Vocoder 📢
Tiger works better with the hifi-gan vocoder released by [fish-diffusion](https://github.com/fishaudio/fish-diffusion/releases/tag/v2.0.0), however if you prefer the sound of the standard ```nsf-hifigan``` vocoder, you can change the line in ```dsconfig.yaml``` starting with vocoder to: ```vocoder: nsf-hifigan```
### 🖌️ Voice Modes 🖌️
Tiger can use 5 different voice modes currently, here's a quick rundown of each. [This page](link) has more information on each voice mode.<br>

| Voice Mode | Description |
| :---: | :--- |
| ☮️ Fresh ☮️ | is the basic vocal mode. |
| 💃 Disco 💃 | is a softer, calmer vocal mode. |
| 🌩️ Electric 🌩️ | is a strong, shocking vocal mode. |
| 💿 Vinyl 💿 | is a mature, booming vocal mode. |
| ✨ Cetera ✨ | contains data for other languages, such as Japanese and Spanish. Closest to Fresh in tone. |

### ❓ Any issues? ❓
If you run into any issues using Tiger, reach out to me here via the [issues](https://github.com/spicytigermeat/tiger_diffsinger/issues) tab, or by other means such as twitter or discord.

<details>
<summary>🗣️ Phonetic Information 🗣️</summary>
  <br>
  <details>

  <summary>English Specific</summary>
    
  | Vowel | Explaination | Consonant | Explaination |
  | :---: | :---: | :---: | :---: |
  | aa | body [b ***aa*** d iy] | b | bubble [***b*** ah b ax l] |
  | ae | cat [k ***ae*** t] | ch | check [***ch*** eh k] |
  | ah | cut [k ***ah*** t] | d | duty [***d*** uw dx iy] |
  | ao<sup>1</sup> | all [***ao*** l] | dx | butter [b ah ***dx*** er] |
  | aw | out [***aw*** t] | f | fish [***f*** ih sh] |
  | ax<sup>2</sup> | again [***ax*** g eh n] | g | glob [***g*** l aa b] |
  | ay | fly [f l ***ay*** | hh | help [***hh*** eh l p] |
  | eh | get [g ***eh*** t] | jh | joke [***jh*** ow k] |
  | er | her [hh ***er***] | k | calf [***k*** ae f] |
  | ey | play [p l ***ey***] | l | little [***l*** ih dx ax l] |
  | ih | been [b ***ih*** n | m | make [***m*** ey k] |
  | iy | bee [b ***iy***] | n | noodle [***n*** uw dx ax l] |
  | ow | crow [k r ***ow***] | ng | thing [th ih ***ng***] |
  | oy | boy [b ***oy***] | p | price [***p*** r ay s] |
  | uh | good [g ***uh*** d] | r | rice [***r*** ay s] |
  | uw | too [t ***uw***] | s | slay [***s*** l ey] |
  | | | sh | ship [***sh*** ih p] |
  | | | t | tip [***t*** ih p] |
  | | | th | thigh [***th*** ay] |
  | | | v | vibe [***v*** ay b] |
  | | | w | what [***w** ah t] |
  | | | y | yes [***y*** eh s] |
  | | | z | zoo [***z*** uw] |
  | | | zh | asia [ey ***zh*** ah] |
  
  <sup>1</sup>: [ao] is a multiuse phoneme dependant on context. Preceeding [l], it makes "all", but preceeding [r], it makes "or".<br>
  <sup>2</sup>: [ax] is a schwa, which is another multiuse phoneme dependant on context. It creates [el] when it preceeds [ax l], for example.
  
  </details>

 <details>

  <summary>Usage Basics</summary>

  | Phoneme | Name | Explaination |
  | :---: | :---: | :--- |
  | SP | Silence | DiffSinger's label for silence |
  | AP | Breath | DiffSinger's label for breaths |
  | q | Glottal Stop | uh-oh [ah ***q*** ow] |
  | vf | Vocal Fry | Not stable, put it in random spots and see what happens... |
  | cl | Plosive Modifier | Place after a plosive consonant to remove the "pop" if it's unwanted. [w ah t ***cl***] |
   
 </details>

 <details>

  <summary>Non-English Extensions</summary>

  | Phoneme | Type | X-Sampa | Explaination |
  | :---: | :---: | :---: | :--- |
  | ee | vowel | e | Accented 'e', like in Spanish and Japanese |
  | oo | vowel | o | Closed 'o', like in Spanish and Japanese |
  | uu | vowel | u | Closed 'u', like in Spanish and PT-BR |
  | ux | vowel | M | Japanese 'u' |
  | hx | cons. | x | Spanish 'j', like in 'ojos' [oo hx oo s] |
  | rr | cons. | rr | Rolled R, like in perrito [p ee rr iy tx oo] |
  | rx | cons. | R | Uvular R, like in 'Março' [m aa rx s] |
  | tx | cons. | t | Unaspirated t. For Non-English languages |
   
 </details>

</details>

<details>

  <summary>📊 Model Information 📊</summary>
Trained as a multispeaker model, total model time is roughly 3.5 hours. Tiger occupies about half of that data in this build.

| Acoustic Model | 📢 |
| --- | --- |
| Steps | 40K |
| Epochs | 206 |
| aux_mel loss | 0.0087 |
| mel loss | 0.0523 |
| val loss | 0.1873 |

| Duration Model | 📏 | Pitch Model | 📈 |
| --- | --- | --- | --- |
| Steps | 120K | Steps | 170K |
| Epochs | 618 | Epochs | 876 |
| Loss | 0.0032 | Loss | 0.0003 |
  
</details>

