        //\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
        ||                      DRAGONFLY CODE STYLE                     ||
        \\///////////////////////////////////////////////////////////////

                                       (\"/)                                        (/|\)
                                         |
                                         |

# Table of Contents

- [Indentation and Formatting](#indentation-and-formatting)
- [Naming Conventions](#naming-conventions)
- [Imports](#imports)
- [Comments and Documentation](#comments-and-documentation)
- [Function and Method Definitions](#function-and-method-definitions)

## Indentation and Formatting

- **Indentation:**
   - Use 4 spaces for each level of indentation (avoid tabs). 
  - Don't mix tab with spaces
  - Maximum Line length should be 79 spaces. 

   - Good:
     ```python
     def my_function():
         if condition:
             print("Condition is True")
         else:
             print("Condition is False")
     ```

   - Avoid:
     ```python
     def my_function():
     	if condition:
     		print("Condition is True")
     	else:
     		print("Condition is False")
     ```

- **Line Length:**
   - Follow the PEP 8 recommended line length of 79 characters for code.
   - If a line exceeds the limit, break it before operators or after commas.
   - Good:
     ```python
     def long_function_name(
         parameter1, parameter2, parameter3, parameter4
     ):
         return parameter1 + parameter2 + parameter3 + parameter4
     ```

   - Avoid:
     ```python
     def long_function_name(parameter1, parameter2, parameter3, parameter4): return parameter1 + parameter2 + parameter3 + parameter4
     ```

- **Whitespace:**
   - Use a single space after commas in function calls and before and after binary operators.
   - Good:
     ```python
     result = function_call(arg1, arg2)
     total = num1 + num2
     ```

   - Avoid:
     ```python
     result = function_call(arg1,arg2)
     total = num1+num2
     ```

- **Wrapping Lines:**
   - When a line is too long, prefer breaking before operators or after commas.
   - Good:
     ```python
     total = (num1 +
              num2 +
              num3)
     ```

   - Avoid:
     ```python
     total = (num1 + num2
              + num3)
     ```

## Naming Conventions

Approved variable styles:
    lowercase
    lower_case_with_underscores
    UPPERCASE
    UPPER_CASE_WITH_UNDERSCORES
    CapitalizedWords 
    
- **Variables, Functions, and Modules:**
  - Use lowercase letters.
  - Separate words with underscores to improve readability using lower_case_with_underscores.
  - Examples: `my_variable`, `calculate_area`, `my_module.py`

  - **Arrays:**
  - Use plural names for variables representing arrays or lists.
  - Examples: `students`, `cars`, `fruits`

  - **Object Arrays (List of Objects):**
    - Use plural names for variables representing lists of objects.
    - Each element in the list should be a singular noun, describing the individual object type.
    - Examples: `users`, `articles`, `employees`

- **Classes:**
  - Use CapitalizedWords, starting with an uppercase letter for each word.
  - Examples: `MyClass`, `PersonInfo`, `DatabaseManager`

- **Constants:**
  - Use UPPERCASE letters.
  - Separate words with UPPER_CASE_WITH_UNDERSCORES to improve readability.
  - Examples: `PI`, `MAX_COUNT`, `CONFIG_FILE`

- **Private Variables and Functions:**
  - Use a single leading underscore before the name.
  - Example: `_private_variable`, `_private_function`

- **Protected Variables and Functions:**
  - Use a single leading underscore before the name.
  - Example: `_protected_variable`, `_protected_function`

- **Module-level Constants and Global Variables:**
  - Use UPPERCASE letters.
  - Separate words with UPPER_CASE_WITH_UNDERSCORES to improve readability.
  - Example: `GLOBAL_VARIABLE`, `CONFIGURATION_FILE`

- **Acronyms and Initialisms:**
  - Treat acronyms and initialisms as lowercase in most cases, except if they are the first word in a name, or as a whole are used as a constant.
  - Examples: `url_handler`, `http_request`, `URL`, `HTTP`

- **Environment Variables:**
  - Use descriptive names for environment variables.
  - Use uppercase letters.
  - Separate words with underscores to improve readability.
  - Examples: `API_KEY`, `DATABASE_URL`, `SECRET_KEY`


- **Additional Examples**
    <details>
    <summary>Examples</summary>

    ```python
    # Variables

    user_id = 123
    is_active = True

    # Functions
    def calculate_sum(a, b):
        return a + b

    # Constant Variables
    MAX_ATTEMPTS = 5
    PI = 3.14159

    class AzureAdUser:
        pass

    class AuvikAlert:
        pass

    AZURE_USERNAME = os.environ.get('USERNAME')
    NABLE_PASSWORD = os.environ.get('PASSWORD')
    ```
    </summary>

## Imports

- **Import Order:**
  - Imports should be grouped in the following order:
    1. Standard library imports
    2. Related third-party imports
    3. Local application/library-specific imports

- **Explicit Imports:**
  - Avoid wildcard imports (`from module import *`).
  - Import only the specific functions, classes, or variables needed from a module.
  - Good:
    ```python
    import os
    import numpy as np
    from my_module import MyClass, my_function
    ```

  - Avoid:
    ```python
    from my_module import *
    ```
- **Line Breaks for Long Imports:**
  - When importing multiple modules from a single package, break the imports into multiple lines for better readability.
  - Good:
    ```python
    from very_long_module_name import (
        first_item,
        second_item,
        third_item,
        fourth_item,
    )
    ```

  - Avoid:
    ```python
    from very_long_module_name import first_item, second_item, third_item, fourth_item
    ```

- **Aliases for Long Module Names:**
  - If a module name is long, use an alias to shorten it.
  - Good:
    ```python
    import pandas as pd
    import matplotlib.pyplot as plt
    ```

  - Avoid:
    ```python
    import this_is_a_very_long_module_name as tialmn
    ```

- **Unused Imports:**
  - Remove any unused imports from the code.
  - Unused imports clutter the code and may lead to confusion.

- **Imports Placement:**
  - Place imports at the top of the file, before any other code.
  - Separate imports from the rest of the code with two blank lines.

- **Importing Modules in Functions:**
  - Avoid importing modules inside functions, as it can negatively impact performance.
  - Move the import statements to the top of the file.

- **Importing Submodules:**
  - If possible, import only the required submodules from a package instead of the entire package.
  - Good:
    ```python
    from math import pi
    ```

  - Avoid:
    ```python
    import math
    ```
  - Adittional Examples:
    -<details><summary>Examples</summary>
    ```python
        # Standard Library Imports
    import os
    import sys
    from datetime import datetime
    import logging

    # Related Third-Party Imports
    import numpy as np
    import pandas as pd
    from matplotlib import pyplot as plt
    import requests

    # Local Application/Library-specific Imports
    from my_app.models import User, Product
    from my_app.utils import validate_input
    from my_app.config import API_KEY, DATABASE_URL
    ```
    </summary>

    Good:
    ```Python
    import pandas as pd from elasticsearch import Elasticsearch
    def dragonfly_exporter(dataframe: pd.DataFrame, elastic_host: str, index_name: str) -> None:
        """
        Export a DataFrame to Elasticsearch.

        Args:
            dataframe (pd.DataFrame): The DataFrame to be exported.
            es_host (str): The Elasticsearch host URL.
            index_name (str): The name of the index in Elasticsearch.
        """

        elastic_client = Elasticsearch(elastic_host)
        if elastic_client.connect():
            print("Connected to Elasticsearch.")
        else:
            print("Failed to connect to Elasticsearch.")
            return

        # Document Complex Logic
        for _, row in dataframe.iterrows():
            document = row.to_dict()
            elastic_client.index(index=index_name, body=document)
            elastic_client.complex_logic()

    ```
    Avoid: 
    ```Python
    import pandas as pd
    from elasticsearch import Elasticsearch

    def dragnonfly_eX(dataframe, elastic_host, i_name):
        """
        Exportar DataFrame a Elasticsearch.
        """

        es = Elasticsearch(elastic_host)
        if es.connect():
            print("Connected to Elasticsearch.")
        else:
            print("Failed to connect to Elasticsearch.")
            return

        print("Llegoo!")
        # Comentario TODO en español.

        # test = {
        #'ID': [1, 2, 3],
        #'Nombre': ['Alice', 'Bob', 'Charlie'],  #
        #'Edad': [25, 30, 22]}
        
        for _, casa in dataframe.iterrows():
            document = casa.to_dict()
            es.index(index=i_name, body=document)
            es.complex_logic()

    ```

