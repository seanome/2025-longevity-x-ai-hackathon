# 2025-longevity-x-ai-hackathon
Base repo for code to clean and upload datasets for Longevity x AI Hackathon June 14-15, 2025 https://lu.ma/a2ag12ya

# Hugging Face Setup

Upload your dataset to our hugging face org!

Structure your dataset like. We are requiring parquet as the final format for standardization.

```
dataset_name/
├── train.parquet
├── test.parquet
└── dataset_infos.json (optional)
```

Be sure to fill out the dataset card with details about where the data originated from!

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
