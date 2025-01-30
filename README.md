# Naruto-Anime-Character-Network

## Overview
This project analyzes character relationships in a dataset containing subtitle files. It extracts named entities from dialogues and visualizes their interactions as a character network.

## Dataset
- The project uses subtitle files (`.ass` format) stored in `../data/Subtitles/`.
- Dialogue text is extracted from these files for further analysis.

## Steps and Methods
### 1. Data Loading
- Subtitle files are read and processed to extract dialogues.

### 2. Named Entity Recognition (NER)
- Uses **spaCy (`en_core_web_trf`)** to identify characters (PERSON entities) in dialogues.

### 3. Sentence Tokenization
- Uses **NLTK (`sent_tokenize`)** to split dialogues into sentences for precise entity extraction.

### 4. Building a Character Network
- Constructs a graph using **NetworkX**, where:
  - Nodes represent characters.
  - Edges represent co-occurrences within the same sentences.

### 5. Visualization
- Generates static visualizations using **Matplotlib**.
- Creates interactive network displays using **Pyvis**.
