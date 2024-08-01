## README

### Overview

In this project, I will be working with a typical annotation file used in computational biology. The tasks include retrieving and parsing the file, converting columns to appropriate data types, writing parsed contents to a JSON file, counting protein-coding genes per chromosome, and creating a visualization of the counts. This README provides a step-by-step guide to the implementation.

### Steps

1. **Retrieve the File from Provided URI**
   - The file is located at: [Homo_sapiens.gene_info.gz](https://ftp.ncbi.nlm.nih.gov/gene/DATA/GENE_INFO/Mammalia/Homo_sapiens.gene_info.gz)
   - This file is in a compressed format (`.gz`).

2. **Parse the File into a Suitable In-Memory Data Structure**
   - The file will be parsed using a data frame library like `pandas`.

3. **Convert Each Column to an Appropriate Data Type**
   - Relevant columns for this task are `type_of_gene` and `chromosome`.
   - Ensuring these columns have the correct data types will be crucial for accurate data analysis.

4. **Write the Parsed Contents Out to a New File, in JSON Format**
   - The parsed data will be written to a new JSON file for easier manipulation and future use.

5. **Produce a Count of the Number of Protein-Coding Genes on Each Chromosome**
   - Using the `type_of_gene` and `chromosome` columns, I will count the number of protein-coding genes for each chromosome.

6. **Create a Visualization of the Per-Chromosome Protein-Coding Gene Counts**
   - I will use a visualization library like `matplotlib` or `seaborn` to create a visual representation of the gene counts.

### Implementation Details

1. **Retrieving the File**
   - I will use the `requests` library to download the file.
   - The file will be decompressed using the `gzip` library.

2. **Parsing the File**
   - I will read the decompressed file into a `pandas` DataFrame.
   - The README file available at: [README](https://ftp.ncbi.nlm.nih.gov/gene/DATA/README) provides useful information on the file structure.

3. **Data Type Conversion**
   - I will ensure the `type_of_gene` and `chromosome` columns are in the appropriate data types (`str`).

4. **Writing to JSON**
   - The parsed DataFrame will be written to a JSON file using `pandas`' `to_json` method.

5. **Counting Protein-Coding Genes**
   - I will filter the DataFrame to include only rows where `type_of_gene` is `protein-coding`.
   - Using `groupby` and `size` functions, I will count the number of protein-coding genes per chromosome.

6. **Creating a Visualization**
   - The counts will be visualized using `matplotlib` or `seaborn` to produce a bar chart.

### Dependencies

- Python 3.x
- pandas
- requests
- gzip
- matplotlib or seaborn

### Usage

1. **Install Dependencies**
   ```sh
   pip install pandas requests matplotlib seaborn
   ```

2. **Run the Script**
   - Ensure the script file is in your working directory.
   - Execute the script:
     ```sh
     python script_name.py
     ```

### Best Practices

- The code employs real-world best practices, including:
  - Data type validation
  - Effective documentation
  - Use of context managers for file handling
  - Error handling for network requests and file operations

### Conclusion

This project demonstrates the use of Python for data retrieval, parsing, transformation, and visualization in the context of computational biology. The script is designed to be efficient and easy to understand, following best practices in software development.

