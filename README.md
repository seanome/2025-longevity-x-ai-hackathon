# 2025-longevity-x-ai-hackathon
Base repo for code to clean and upload datasets for Longevity x AI Hackathon June 14-15, 2025 https://lu.ma/a2ag12ya

# Hugging Face Setup

Upload your dataset to our hugging face org!

Structure your dataset something like:
```
dataset_name/
├── expression.parquet
├── feature_metadata.parquet
├── processing_script.py
└── dataset_infos.json (optional)
``` 

ℹ️ We are requiring parquet as the final format for standardization!

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

### Example HuggingFace Submission

Here is an example of a nicely formatted HuggingFace submission: https://huggingface.co/datasets/longevity-db/tabula-muris-senis-bladder-smartseq2
