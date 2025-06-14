# 2025-longevity-x-ai-hackathon
Base repo for code to clean and upload datasets for Longevity x AI Hackathon June 14-15, 2025 https://lu.ma/a2ag12ya

# Hugging Face Setup

Upload your dataset to our hugging face org!

Structure your dataset like
```
dataset_name/
├── train.csv
├── test.csv
└── dataset_infos.json (optional)
```

Preferred formats:

- CSV (.csv)
- JSON (.json, .jsonl)
- Parquet (.parquet) ← preferred for large/tabular data
- Arrow (.arrow) ← internal optimized format
- Text (.txt) for plain corpora
- Image/audio/video files with metadata in .csv/.json

You can request to join the org as a contributor with ***REMOVED***

For the duration of the hackathon we will provide you with a temporary write permission token (ask us) to accelerate the process.

```bash
pip install datasets huggingface_hub
huggingface-cli login # (Ask us for a temporary token)
huggingface-cli repo create my_dataset --repo-type dataset --organization longevity-db
huggingface-cli upload longevity-db/my_dataset . --repo-type=dataset
```

Then you can interact with it like a normal git repo!

```bash
git clone git://huggingface.co/datasets/longevity-db/test_dataset
```
