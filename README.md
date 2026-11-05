# Accurate-Salamander Grand Piano 6.2a — MP3 conversion

MP3 conversion of a subset of **Accurate-Salamander Grand Piano 6.2a** by cyamauch
(https://www.ir.isas.jaxa.jp/~cyamauch/AccurateSalamander/), which is based on
**Salamander Grand Piano V3** by Alexander Holm
(https://archive.org/details/SalamanderGrandPianoV3).

## License

CC BY 3.0 (https://creativecommons.org/licenses/by/3.0/), same as the original.
The license statement is in `ORIGINAL-README.txt` (section "Licence"), copied unchanged
from the Accurate-Salamander 6.2a package.

## What we changed

Source: `AccurateSalamanderGrandPianoV6.2a_48khz24bit_flac.zip` (48 kHz / 24 bit FLAC).

- Selected velocity layers 5–15 (of 16), at all 30 sample points (A0, C1, D#1, F#1, A1 … C8).
- Main samples and string-resonance samples were cut to the first 8.3 s.
- Encoded with LAME (`--abr 112 -q 2 -m j`), output 44.1 kHz.
- Release (`rel1`–`rel88`), pedal (`pedalD1/2`, `pedalU1/2`) and string-resonance
  (`harmL*`, `harmS*`, `harmV3*`) samples were converted the same way, uncut.
- No other processing (no EQ, no level changes).

## Layout

- `v<N>/<note>v<N>.mp3` — velocity layer N (5–15), e.g. `v11/C4v11.mp3`
- `rel/rel<1–88>.mp3` — key-release noise
- `pedal/pedal{D1,D2,U1,U2}.mp3` — sustain pedal down / up
- `harm/harm{L,S,V3}<note>.mp3` — release string resonance
