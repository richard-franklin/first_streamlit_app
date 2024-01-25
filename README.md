# CONFIG GENERATOR v2.0.0

Streamline the automation of generating configurations for table loading into Snowflake.


## Installation
Use the Python package manager [pip](https://pip.pypa.io/en/stable/) to install the pandas library.
```bash
pip install pandas
```
_The framework has been tested for python versions 3.11 and below._
## Components
Below are the key components of the framework:
1. **input.csv**:<br>
   This CSV file is used to take the necessary details of the tables whose configurations are to be generated.<br>
2. **historical_query_generator.py**:<br>
   This file is run to generate all the configurations needed for the first full load of the table.<br>
3. **incremental_query_generator.py**:<br>
   This file is run to generate all the update queries for the already inserted configurations and also some new configurations.<br>
4. **queries.py**:<br>
   This file contains the templates of all the queries that are to be generated.
   
## Usage
Below are the steps to follow in order to run the framework:
- Step 1: Insert the details of the tables whose configurations are to be generated in the **input.csv** file.
- Step 2: Run the script using the **historical_query_generator.py** (for new entry) or **incremental_query_generator.py**(for after historical load) file.
```bash
python historical_query_generator.py
```
- Step 3: The script execution pauses right at the beginning, prompting to enter either **S** or **D**.
<br>      **S** is entered for generating configurations for master load architecture.
<br>      **D** is entered for those that doesn't use the master load architecture.
- Step 4: The output of each script will be available in either **historical_config** folder or **incremental_config** folder based on the script that was run.
##
