---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.13.8
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

```python
import numpy as np
import matplotlib.pyplot as plt
from IPython.display import Audio
```

# Frequenzen - Pitches - MIDI

| dt. Tonhöhenbez. | scientific pitch notation |    MIDI | Freq. (Hz) |
| ---------------- | ------------------------- | ------- | ---------- |
|               a' |                        A4 |      69 |        440 |
|              a'' |                        A5 | 69 + 12 | $440 \cdot 2$ |
|                a |                        A3 | 69 - 12 | $440 \cdot \dfrac{1}{2}$ |
|             ais' |                       A#4 |  69 + 1 | $440 \cdot 2^{\frac{1}{12}}$ |
 
--> enharmonische Verwechslung per Design

Multiplikator für die Erhöhung einer Frequenz um einen Halbton (im westl. zwölftönigen temperierten Stimmungssystem)

$f \cdot 2^{\frac{1}{12}}$

```python
def midi_to_freq(pitch, freq_reference=440, pitch_reference=69,
                 num_divisions_per_octave=12):
    
    return freq_reference * (2 ** ((pitch - pitch_reference) / num_divisions_per_octave))
```

```python
print(midi_to_freq(69))
print(midi_to_freq(69 + 12))
print(midi_to_freq(69 - 12))
print(midi_to_freq(69 + 1))
print(midi_to_freq(60))
print(midi_to_freq(69 + 0.5)) # viertelton nach oben
```
