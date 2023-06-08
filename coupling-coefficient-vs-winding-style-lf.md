# Coupling Coefficient vs. Winding Style (Low Frequency)

I performed a few basic tests of transformer winding styles to determine their
influence on the transformer's coupling coefficient and inter-winding
capacitance.

I used the same transformer core for all measurements to make sure that the core
material parameter variance did not interfere with the results. In all cases
except when air gaps were added on purpose, the transformer windings were
tightly wound on the core. However, no extra efforts to completely eliminate the
air gaps underneath the winding were taken, which should represent a reasonably
well-made transformer.

I used an LCR meter to make two measurements of the primary winding inductance.
The first measurement (Lo) was performed with the secondary winding open, while
the second measurement (Ls) was with the secondary winding shorted. The coupling
coefficient was then calculated as **K = sqrt ((Lo - Ls) / Lo)**, where **sqrt**
is the square root.

The same LCR meter was used to measure the inter-winding capacitance. Both
windings were shorted during the measurement.

Although the measurements were performed on a single, relatively low frequency
of 100 kHz, the results still seem useful for choosing the winding strategy and
as a baseline for further research. VNA measurements over the entire frequency
range of interest would have offered a better insight into the coupling
coefficient behaviour but are considerably more challenging to perform and
interpret correctly. Thus, measuring the coupling coefficient on a VNA was left
for the future.

## Transformer Details

Core Type: [Amidon FT-140-43](https://www.amidoncorp.com/ft-140-43/) toroidal core  
Wire: 0.5 mm enameled round copper wire  
Primary Turns: 8  
Secondary Turns: 8  
Winding style: varies, see below

## Measurement Equipment and Conditions

LCR Meter: [CEM LT-9935 Digital
LCR-meter](https://www.cem-instruments.com/en/product-id-1147)  
Calibration: built-in open/short calibration performed prior to each transformer
measurement  
Measurement frequency: 100 kHz

## Winding Styles

Below are the descriptions of the winding styles I tested.

### Separated Windings

Primary and secondary windings are wound on opposite sides of the core.

![Separated Windings
Pictire](./coupling-coefficient-vs-winding-style-lf/separated-windings.jpg
"Separated Windings")

### Evenly Spaced Windings

Primary and secondary windings are evenly spaced on the core.

![Evenly Spaced Windings
Pictire](./coupling-coefficient-vs-winding-style-lf/evenly-spaced-windings.jpg
"Evenly Spaced Windings")

### Bifilar Windings

The classic bifilar winding style. Windinga are evenly spaced on the core.

![Bifilar Windings
Pictire](./coupling-coefficient-vs-winding-style-lf/bifilar-windings.jpg
"Bifilar Windings")

### Loosely Twisted Windings

Primary and secondary windings are twisted at the rate of 120 twists per meter
and evenly spaced on the core.

![Loosely Twisted Windings
Picture](./coupling-coefficient-vs-winding-style-lf/loosely-twisted-windings.jpg
"Loosely Twisted Windings")

### Tightly Twisted Windings

Primary and secondary windings are twisted at the rate of 360 twists per meter
and evenly spaced on the core.

![Tightly Twisted Windings
Picture](./coupling-coefficient-vs-winding-style-lf/tightly-twisted-windings.jpg
"Tightly Twisted Windings")

### Evenly Spaced Loosely Wound Windings

Primary and secondary windings are evenly spaced and loosely wound on the core
with significant air gaps between the core and the windings.

![Evenly Spaced Loosely Wound Windings
Picture](./coupling-coefficient-vs-winding-style-lf/evenly-spaced-loosely-wound.jpg
"Evenly Spaced Loosely Wound Windings")

### Tightly Twisted Loosely Wound Windings

Primary and secondary windings are twisted at the rate of 330 twists per meter,
evenly spaced and loosely wound on the core with significant air gaps between
the core and the windings.

![Tightly Twisted Loosely Wound Windings
Picture](./coupling-coefficient-vs-winding-style-lf/tightly-twisted-loosely-wound.jpg
"Tightly Twisted Loosely Wound Windings")

## Measurement Results

| Winding Style                 | Lo (uH) | Ls (uH) | K     | C (pF) |
|-------------------------------|---------|---------|-------|--------|
| Separated                     | 52.45   | 5.946   | 0.942 | 2.0    |
| Evenly Spaced                 | 51.11   | 0.585   | 0.994 | 5.4    |
| Bifilar Winding               | 51.33   | 0.337   | 0.997 | 22.1   |
| Loosely Twisted               | 51.24   | 0.532   | 0.995 | 26.6   |
| Tightly Twisted               | 50.56   | 0.262   | 0.997 | 39.4   |
| Evenly Spaced Loosely Wound   | 51.65   | 0.919   | 0.991 | 5.2    |
| Tightly Twisted Loosely Wound | 51.10   | 0.334   | 0.997 | 33.1   |
