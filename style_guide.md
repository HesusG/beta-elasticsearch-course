## //\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
## ||           DRAGONFLY CODE STYLE        ||
##  \\////////////////////////////////


# Table of Contents
-[Naming Conventions](#naming-convention)
-[Code Smells](#code-smells)

## Naming Conventions

Defaults:
    lowercase
    lower_case_with_underscores
    UPPERCASE
    UPPER_CASE_WITH_UNDERSCORES
    CapitalizedWords 

### Attribute Names (variables, properties, functions)

Use lower_case_with_underscores except when using constants, you should use UPPERCASE

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
```


### Class Names
- CapitalizedWords
- Singular Name
- Exporter Tool Name and Object Name

```python
class AzureAdUser:
    pass

class AuvikAlert:
    pass
```
auvik_alert = module.AuvikAlert()

### Object Arrays 

should be plural



### Environment Variables

- Use UPPERCASE for the variable name write tool name at the beggining. 
- Names should be descriptive and should use abbrevations. 

```python
AZURE_USERNAME = os.environ.get('USERNAME')
NABLE_PASSWORD = os.environ.get('PASSWORD')
```

### Code Comments
- Use comments for complex algorithmns and logics, be clear and consice but keep comments at minimum avoiding redudants commnets. 
- Use Docstrings for functions

```python
def calculate_area(radius: float) -> float:
    """
    Calculate the area of a circle given its radius.
    """
    area = 3.14159 * radius ** 2
    return area
```
- Avoid `To Do` comments
- Comment before the code you regef to, not after it.
- Never comment codeblos with the intention of preserving or storing this code, code shoulde be eliminated.
- Comments should only use the english language.


### Code Lay-Out

### Indentantion

- 4 Spaces per indentation
- No extra indentation

- Closing brace/bracket/parenthesis
```python 
my_list = [
    1, 2, 3,
    4, 5, 6,
    ]
```
- Don't mix tab with spaces
- Maximum Line length should be 79 spaces. 

### Imports
- Imports should be on separate lines: 
```python
# Correct:
import os
import sys
# Wrong:
import sys, os
```
- Imports are always put at the top of the file, just after any module comments and docstrings, and before module globals and constants.
- Imports should be grouped in the following order:
- Standard library imports.
- Related third party imports.
- Local application/library specific imports.




### Odoo Specifics 
 _id
 _ids