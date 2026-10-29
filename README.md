# Interactive Cell Atlas

A self-contained 3D cell explorer: click any organelle to read the biochemistry that
happens there, click any link to see how that chemistry reaches another compartment,
and zoom into the nucleus to descend five levels of structure down to nucleosomes.

**[Open the live version](https://USERNAME.github.io/REPO/)** &nbsp;·&nbsp; or download
`index.html` and double-click it — it runs offline with nothing to install.

## What's in it

- **17 compartments** — plasma membrane, cytosol, cytoskeleton, nucleus, nucleolus,
  rough and smooth ER, Golgi, ribosomes, mitochondria, peroxisomes, lysosomes,
  endosomes, autophagosomes, proteasome, lipid droplets, centrosome
- **85 pathway groups / 341 reaction equations** with enzymes, EC numbers, cofactors,
  the regulatory logic that sets flux, and the associated disease or drug where one exists
- **56 inter-organelle connections** in 7 classes (metabolite shuttle, vesicular transport,
  membrane contact site, signalling, protein targeting, gene expression, ion flux)
- **13 pathway spotlights** that trace one pathway across several organelles — glucose
  oxidation, lipogenesis, fasting ketogenesis, gluconeogenesis, the secretory route,
  LDL/SREBP feedback, autophagy flux, the urea cycle, haem, plasmalogens, the Ca²⁺
  circuit, NADPH/redox, mitochondrial biogenesis
- **Nuclear deep zoom** — envelope → chromosome territories and nucleolar subzones →
  nuclear pore complexes and the 30 nm fibre → nucleosomes, B-DNA and RNA Pol II

## Controls

| | Desktop | Touch |
|---|---|---|
| Rotate | drag | one finger |
| Zoom | scroll wheel | pinch |
| Pan | shift-drag or right-drag | two fingers |
| Select | click an organelle or link | tap |
| Cytosol | click empty space | tap empty space |
| Reset | `R` or the Reset button | View → Reset |

On phones the side panels become bottom sheets reached from the tab bar.
Append `?debug` to the URL for an fps / draw-call / triangle readout.

## A note on scale

One world unit is one micrometre. Structures inside the nucleus below ~1 µm are modelled
at **true scale** — nucleosomes really are 11 nm discs wrapped by 147 bp of DNA, the
pore complex ring really is 120 nm, the double helix has a 3.4 nm pitch. Above that level,
organelle sizes are **schematic**: a ribosome drawn at its real 25 nm would be invisible
next to a 6 µm nucleus. The on-screen scale bar is computed from the camera each frame,
so it always reports the true field of view.

## Accuracy

Content is written from standard biochemistry and cell-biology sources as a teaching
reference; it is not machine-extracted from a database and carries no per-statement
citations. Corrections are welcome via issues or pull requests.

## Browser support

Any browser with WebGL: Chrome, Edge, Firefox, Safari 15+. A blank screen almost always
means hardware acceleration is disabled in browser settings.

## Licence

Code and content in this repository are released under the MIT Licence — see `LICENSE`.

This project bundles **three.js v0.160.1** (MIT, © 2010-2023 three.js authors), embedded
in minified form inside the HTML file. Its required notice is reproduced at the top of
`index.html` and in `THIRD_PARTY_NOTICES.txt`.
