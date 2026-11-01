# Data

**File:** `pokemon.csv` (1,351 rows, 20 columns)

**Source:** Kaggle, *Pokemon Stats Dataset*
https://www.kaggle.com/datasets/shreyashautomation/pokemon-stats-dataset

**Licence:** TODO - copy the licence shown on the Kaggle dataset page here and confirm that it permits academic use / redistribution. If it does not permit redistribution, remove `pokemon.csv` from the repo and replace this with download instructions.

**Citation:** TODO - add the dataset author, title, year and URL in the format your lecturer requires.

## Columns used
Features: `height_dm`, `weight_hg`, `hp`, `attack`, `defense`, `special_attack`, `special_defense`, `speed`, `type_1`, `type_2`, `generation`
Target: `is_legendary`

## Columns deliberately not used
`id`, `name` (identifiers); `capture_rate`, `base_experience` (near-proxies for the target, so leakage); `is_mythical` (separate class of special Pokémon); `abilities`, `color`, `shape` (not in the proposed feature set).

## Preparation notes
- Missing `type_2` (single-type Pokémon) is encoded as `"none"`.
- No rows are dropped. Alternate forms (e.g. `deoxys-normal`) appear as separate rows.
