# Medical Document Analysis and Summary Generation System
## Learn-from-feedback

This repository contains a Python script for analyzing medical summary documents and generating concise summaries using OpenAI's GPT-4 model. The script first extracts text from `.docx` files, performs a comparative analysis to identify template updates, and then generates a summary template. The identified pattern together with the updated sections, are then used to create a summarized version of a given medical transcript using the template.
In this way, new sections are taken into consideration, and there's no need to constantly update manually each time.

## Usage

1. **Setup**: Place your `.docx` files that represents the summaries  in the `summaries` folder and ensure you have your OpenAI API key set up in the `.env` file.
2. **Run the Script**: Execute the script to perform the analysis and generate summaries.


## Prerequisites

Before running the script, ensure you have the following dependencies installed:

- Python 3
- `python-docx` (`pip install python-docx`)
- `openai` (`pip install openai`)
- `python-dotenv` (`pip install python-dotenv`)

You also need an OpenAI API key, which should be stored in a `.env` file as `API_KEY`.



## Limitations

- The system currently works with English language documents.
- You have to manually switch the language
- Requires an active OpenAI API key for operation.

## NOTES
  - The idea behind is that the whole process takes place while the user (doctor) is not online, since it requires time to find the common patterns for each summary. Also, the more the files the longer the analysis.
  - In this notebook, it was done imagining that each user (each doctor) has his ‘style’. Of course, a parallel approach could be done also in case the doctor has a different template per patient.

## Script Workflow

```plaintext
1. The script reads `.docx` files from the `summaries` folder.
2. Performs a comparative analysis to identify potential template updates.
3. Generates a summary template based on the analysis.
4. Summarizes a provided medical transcript using the generated template.




