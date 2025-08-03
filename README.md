
# Simple Search Engine

A simple search engine that uses simple Python data structures to store the data and search for it.

## Usage

1. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
````

2. **Prepare the data**
   The data should be free text and in the `data` folder. Every file in the `data` folder will be indexed as a document.

3. **Run the search engine**

   ### On Linux/macOS

   Open terminal, go to the root directory of the project and run:

   ```bash
   export PYTHONPATH=$(pwd)
   python src/main.py
   ```

   ### On Windows (PowerShell)

   Open PowerShell, go to the root directory of the project and run:

   ```powershell
   $env:PYTHONPATH = (Get-Location)
   python src\main.py
   ```

4. **Search for a query**
   The search engine will ask you to enter a query. Enter the query and press enter. The search engine will return the top 5 results.

## How it works

The search engine uses a few simple steps to search for a query:

* It reads the data from the `data` folder and stores it in a dictionary.
* It preprocesses the data by removing stop words, punctuations, numbers and converting the text to lowercase.
* It reads stopwords from the `stopwords.txt` file, preprocesses the stopwords and stores them in a list.
* It reads the query from the user and preprocesses it.
* It calculates the score of each document for the query and ranks them in descending order. The score is calculated by the number of times the document contains the query words.
* It returns the top 5 results.


