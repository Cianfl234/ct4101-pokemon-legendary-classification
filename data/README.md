# Data

**File:** `pokemon.csv` (1,351 rows, 20 columns: 1,025 main species plus 326 alternate forms such as Mega and regional forms)

**Source:** Kaggle, *Pokemon Stats Dataset*, uploaded by `shreyashautomation`
https://www.kaggle.com/datasets/shreyashautomation/pokemon-stats-dataset
(accessed 23 November 2026)

**Original source of the data:** PokéAPI, https://pokeapi.co (the Kaggle description says the data was taken from it).

## Licence
The Kaggle page states **MIT License**. It redistributes the data, so the full notice shown on the page is reproduced here as the licence requires:

```
Released under MIT License

Copyright (c) 2013 Mark Otto.
Copyright (c) 2017 Andrew Fong.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

**Caveats:** the copyright holders named in this notice do not match the Kaggle uploader's username, so the notice may have been copied from another project, and I could not confirm who holds the rights in the data. The underlying Pokémon information (names, types, base stats) comes from the Pokémon games, which belong to Nintendo, Game Freak, Creatures and The Pokémon Company. The data is used here only for academic, non-commercial coursework. If the dataset's licence is a concern, delete `pokemon.csv` and download it from the Kaggle page above into `data/pokemon.csv`. PokéAPI describes itself as free and open to use and primarily an educational tool, with a fair use policy, and it covers the Pokémon video game franchise; I have not found a separate data licence on PokéAPI, so the Kaggle MIT notice above is the only licence stated for this file.

## Citation
shreyashautomation. *Pokemon Stats Dataset*. Kaggle. https://www.kaggle.com/datasets/shreyashautomation/pokemon-stats-dataset (accessed 23 November 2026).

Underlying data: PokéAPI. https://pokeapi.co (accessed 23 November 2026).

## Columns used
Features: `height_dm`, `weight_hg`, `hp`, `attack`, `defense`, `special_attack`, `special_defense`, `speed`, `type_1`, `type_2`, `generation`
Target: `is_legendary`

## Columns deliberately not used
`id`, `name` (identifiers); `capture_rate`, `base_experience` (near-proxies for the target, so leakage); `is_mythical` (separate class of special Pokémon); `abilities`, `color`, `shape` (not in the proposed feature set).

## Preparation notes
- Missing `type_2` (single-type Pokémon) is encoded as `"none"`.
- No rows are dropped. Alternate forms (e.g. `deoxys-normal`, `charizard-mega-x`) appear as separate rows, which is why notebook 03 also runs a grouped cross-validation by species.
- Mythical Pokémon are labelled not Legendary in this data even though their stats are similar, which adds label noise.
