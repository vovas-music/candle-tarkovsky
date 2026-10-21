# Свеча (Candle)

Track 6 of 7 on «Ностальгия» (_Nostalgiya_, “Nostalgia”), the album by Полуживые (_Poluzhivye_), on poems by Arseny Tarkovsky. The poem is «Меркнет зрение — сила моя».

On the site: https://vovazakharov.com/music/candle-tarkovsky

## Files

- `candle-tarkovsky_mix.mp3` — the mix, unmastered: what the master was made from.
- `Полуживые - Свеча.mp3` — the master. The mix survives only as an mp3, so the master is one too.
- `mastering/` — the script that made the master: `master.py`, the `spectrum.py` it imports, and their `requirements.txt`.

## How it was mastered

```sh
pip install -r mastering/requirements.txt
python mastering/master.py candle-tarkovsky_mix.mp3 ref.flac candle-tarkovsky.mp3
```

with `ffmpeg` on `PATH` and the reference below saved as `ref.flac`. Half
strength (`master.py`'s default): Matchering matches the mix to the reference,
half of the EQ difference goes onto the mix, and a limiter keeps the decoded
file under -1 dBTP. `master.py`'s docstring has the whole chain.

## The reference

“In the Flesh”, GENERATED, from “Ghosts of Flesh”, at [vovas-music/intheflesh@a9f3a99](https://github.com/vovas-music/intheflesh/blob/a9f3a99c0af385229480a8f2882df90b2d1f57ed/GENERATED%20-%20In%20the%20Flesh.flac) — raw download:
https://raw.githubusercontent.com/vovas-music/intheflesh/a9f3a99c0af385229480a8f2882df90b2d1f57ed/GENERATED%20-%20In%20the%20Flesh.flac

It was picked blind: three catalogue masters each mastered the mix, and the
operator ranked them unlabelled, loudness-matched, before learning which was
which. It is linked rather than copied here, since it already lives in this
organization.
