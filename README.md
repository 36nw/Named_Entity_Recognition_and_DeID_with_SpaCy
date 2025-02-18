# Named Entity Recognition and De-Identification with SpaCy
# Named_Entity_Recognition_and_DeID_with_SpaCy
This repository contains Python scripts for performing Named Entity Recognition (NER) and De-identification on text using SpaCy. The goal of this project is to extract named entities from text data and then replace personally identifiable information (such as names) with a placeholder ([REDACTED]) to preserve privacy. The project utilizes a news article as an example for NER and de-identification tasks.

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [License](#license)
- [Notes](#notes)

## Overview

This project involves two main tasks:
1. **Named Entity Recognition (NER)**: Identifying and classifying entities (e.g., persons, organizations, dates, etc.) in text using the SpaCy library.
2. **De-identification**: Replacing identified named entities, specifically person names, with "[REDACTED]" to ensure privacy and anonymity.

The script also demonstrates text processing steps such as scraping a webpage for text, counting entities, tokenizing sentences, and visualizing the entities using SpaCy’s built-in visualization tools.

## Installation

Make sure you have Python installed on your machine. You can install the necessary libraries using pip:

```bash
pip install spacy requests beautifulsoup4
python -m spacy download en_core_web_sm
```
This will install:

- **SpaCy:** A powerful NLP library.
- **Requests:** For making HTTP requests to fetch webpage data.
- **BeautifulSoup4:** For parsing HTML and extracting text from webpages.

## Usage

To use this project, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/Named_Entity_Recognition_and_DeID_with_SpaCy.git
    cd Named_Entity_Recognition_and_DeID_with_SpaCy
    ```

2. Install the necessary dependencies by running:

    ```bash
    pip install -r requirements.txt
    ```

    Alternatively, you can manually install the dependencies:

    ```bash
    pip install spacy requests beautifulsoup4
    python -m spacy download en_core_web_sm
    ```

3. Run the Python script that fetches text from a webpage, performs NER, and then de-identifies the person names:

    ```bash
    python ner_and_deid.py
    ```

    This will:
    - Scrape the text from the specified webpage.
    - Perform Named Entity Recognition (NER) using the SpaCy model.
    - De-identify all person names in the text by replacing them with "[REDACTED]".
    - Visualize the entities and the modified text using SpaCy's `displacy` tool.
    
4. Check the output to see:
    - A list of named entities identified in the text.
    - The visualization of the named entities using `displacy`.
    - The de-identified text with person names replaced by "[REDACTED]".
    - A visualization of the de-identified text with the modified entities.

## Data

The data for this project is sourced from a publicly available news article on the NBC News website. The webpage is scraped using the requests and BeautifulSoup libraries to extract the text, which is then processed with SpaCy.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Notes

- This project uses SpaCy's pre-trained model en_core_web_sm. For better accuracy, you may consider using the medium or large models (en_core_web_md or en_core_web_lg).
- The de-identification process in this project only focuses on person names (label "PERSON"). You can extend it to other types of entities (like organizations or locations) by modifying the code.
- Ensure you have Jupyter Notebook or another compatible environment to view the visualizations using displacy.render().

For any questions or issues, please feel free to open an issue or pull request in this repository.

Happy coding!
