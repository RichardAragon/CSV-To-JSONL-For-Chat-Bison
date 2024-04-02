# CSV-To-JSONL-For-Chat-Bison

This is a simple Python script that converts a CSV dataset from Hugging Face into a JSONL format suitable for training a chatbot using Chat Bison.

## Features

- Loads a dataset from Hugging Face using the `datasets` library
- Converts the dataset into a JSONL format compatible with Chat Bison
- Writes the converted data to a JSONL file

## Requirements

- Python 3.x
- `datasets` library (install via `pip install datasets`)

## Usage

1. Replace the `dataset_path` variable with the actual path to your dataset on Hugging Face.
2. Specify the desired output JSONL file name by modifying the `jsonl_file` variable.
3. Run the script using the command: `python csv_to_jsonl.py`

The script will load the dataset from Hugging Face, convert it into the required JSONL format, and save the resulting data to the specified JSONL file.

## JSONL Format

The converted data will be in the following JSONL format:

{"messages": [{"author": "user", "content": "prompt"}, {"author": "assistant", "content": "response"}]}
```

Each line in the JSONL file represents a separate conversation, consisting of a user prompt and the corresponding assistant response.

## Dataset Structure

The script assumes that the input dataset has the following structure:

- The dataset should be available on Hugging Face.
- The dataset should have a 'train' split containing the training data.
- Each row in the 'train' split should have a 'prompt' field and a 'response' field.

Make sure your dataset follows this structure for the script to work correctly.

## License

This script is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).

## Acknowledgements

- The script utilizes the `datasets` library from Hugging Face for loading datasets.
- The JSONL format is compatible with Chat Bison for training chatbots.

Feel free to customize and use this script for converting your CSV datasets to JSONL format for training chatbots with Chat Bison!
