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
### Framework Execution Steps:
1. **Input Details:**
   - Insert table details in the **input.csv** file.
2. **Run Script:**
   - Execute the script using:
```bash
python historical_query_generator.py
```
     or
```bash
python incremental_query_generator.py
```
3. **Script Interaction:**
   - The script pauses at the start, prompting to enter either **S** for master load architecture configurations or **D** for others.
4. **Output Location:**
   - The output is stored in:
     - **historical_config** folder (for historical load script)
     - **incremental_config** folder (for incremental load script).
##
