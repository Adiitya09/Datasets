# Dataset Layout

Medical image datasets are **not** tracked in git. Place your files locally under `data/` using this structure:

```
data/
├── Train/
│   ├── FYP skin disease Dataset/
│   │   ├── Acne/
│   │   ├── Melanoma/
│   │   └── ...
│   ├── Eye disease/
│   │   ├── A/
│   │   ├── C/
│   │   └── ...
│   └── Oral Cancer/
│       ├── CANCER/
│       ├── NON CANCER/
│       └── ...
├── Validation/
│   └── (same domain / class folders as Train)
└── Test/
    └── (same domain / class folders as Train)
```

## Creating Splits

If you have a single raw folder instead of pre-split data, use:

```bash
python scripts/split_medical_dataset.py
```

By default the script reads from `data/raw/` and writes to `data/splits/`. Edit the paths at the top of `scripts/split_medical_dataset.py` if your layout differs.

## Domains

| Key | Folder name | Model output |
|---|---|---|
| `skin` | `FYP skin disease Dataset` | `models/skin_model.keras` |
| `eye` | `Eye disease` | `models/eye_model.keras` |
| `oral` | `Oral Cancer` | `models/oral_model.keras` |
