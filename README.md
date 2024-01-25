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
This CSV file is used to take the necessary details of the tables whose configurations are to be generated.
2. **historical_query_generator.py**:<br>
   This file is run to generate all the configurations needed for the first time full load of the table
3. **incremental_query_generator.py**:<br>
   This file is run to generate all the update queries for the already inserted configurations and also some new configurations.
