.. Copyright 2020-2023 Robert Bosch GmbH

.. Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

.. http://www.apache.org/licenses/LICENSE-2.0

.. Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.

Test Use Cases
==============

* **Test JPP_0001**

  [DATA_TYPES / GOODCASE]

   **JSON file with parameters of different data types (basic and composite)**

   Expected: All values are returned untouched, with their correct data types

----

* **Test JPP_0002**

  [DATA_TYPES / GOODCASE]

   **JSON file containing parameters with dollar operator syntax at right hand side of colon, basic data types**

   Expected: All parameters referenced by dollar operator are resolved correctly, with their correct data types

----

* **Test JPP_0003**

  [DATA_TYPES / GOODCASE]

   **JSON file containing parameters with dollar operator syntax at right hand side of colon, composite data type: list**

   Expected: All parameters referenced by dollar operator are resolved correctly, with their correct data types

----

* **Test JPP_0005**

  [DATA_TYPES / GOODCASE]

   **JSON file with string values containing dollar operators**

   Expected: All parameters referenced by dollar operator are resolved correctly, outcome is a string containing the values of all referenced parameters

----

* **Test JPP_0100**

  [DATA_INTEGRITY / GOODCASE]

   **JSON file is empty (single pair of brackets only)**

   Expected: JsonPreprocessor returns empty dictionary

----

* **Test JPP_0101**

  [DATA_INTEGRITY / GOODCASE]

   **JSON file with string containing several separator characters and blanks; no parameters**

   Expected: String is returned unchanged

----

* **Test JPP_0102**

  [DATA_INTEGRITY / GOODCASE]

   **JSON file with string containing more special characters, masked special characters and escape sequences**

   Expected: String is returned unchanged (but with masked special characters and escape sequences resolved)

----

* **Test JPP_0200**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / string parameter substitution in parameter value**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0201**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / string parameter substitution in parameter name**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0202**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / index parameter substitution in parameter name / standard notation**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0203**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / index parameter substitution in parameter name / dotdict notation**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0204**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / index parameter substitution in parameter value / standard notation**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0205**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / index parameter substitution in parameter value / dotdict notation**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0206**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / key parameter substitution in parameter name / standard notation**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0207**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / key parameter substitution in parameter name / dotdict notation**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0208**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / key parameter substitution in parameter value / standard notation**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0209**

  [PARAMETER_SUBSTITUTION / GOODCASE]

   **JSON file with nested parameter / key parameter substitution in parameter value / dotdict notation**

   Expected: JsonPreprocessor creates a new string with all dollar operator expressions resolved as string

----

* **Test JPP_0250**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / string parameter substitution in parameter value / innermost parameter not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0251**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / string parameter substitution in parameter name / in between parameter not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0252**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / index parameter substitution in parameter name / standard notation / index parameter not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0253**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / index parameter substitution in parameter name / dotdict notation / index parameter not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0254**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / index parameter substitution in parameter value / standard notation / index parameter not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0255**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / index parameter substitution in parameter value / dotdict notation / index parameter not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0256**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / key parameter substitution in parameter name / standard notation / variant number not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0257**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / key parameter substitution in parameter name / dotdict notation / milestone number not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0258**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / key parameter substitution in parameter value / standard notation / variant number not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0259**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with nested parameter / key parameter substitution in parameter value / dotdict notation / milestone number not existing**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0261**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with list parameter substitution in parameter name (composite data types not allowed in names) / (2)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0263**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with dictionary parameter substitution in parameter name (composite data types not allowed in names) / (2)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0264**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with list parameter substitution in key name (composite data types not allowed in names) / (1)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0265**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with list parameter substitution in key name (composite data types not allowed in names) / (2)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0266**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with dictionary parameter substitution in key name (composite data types not allowed in names) / (1)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0267**

  [PARAMETER_SUBSTITUTION / BADCASE]

   **JSON file with dictionary parameter substitution in key name (composite data types not allowed in names) / (2)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0300**

  [VALUE_DETECTION / GOODCASE]

   **JSON file with parameter of type 'list' / index (in square brackets) defined outside the curly brackets (valid syntax)**

   Expected: JsonPreprocessor returns values

   *Hint: Checklist rule 1*

----

* **Test JPP_0301**

  [VALUE_DETECTION / GOODCASE]

   **JSON file with expression containing more closing elements '}' than opening elements '${' (valid syntax)**

   Expected: JsonPreprocessor returns values

   *Hint: Checklist rule 3*

----

* **Test JPP_0302**

  [VALUE_DETECTION / GOODCASE]

   **JSON file with expression starting with '${' and ending with '}' / no further matching '${' and '}' in between (valid syntax)**

   Expected: JsonPreprocessor returns values

   *Hint: Checklist rule 4*

----

* **Test JPP_0304**

  [VALUE_DETECTION / GOODCASE]

   **JSON file with expression starting with '${' and ending with '}', further matching '${' and '}' in between (not all nested) (valid syntax)**

   Expected: JsonPreprocessor returns values

   *Hint: Checklist rule 6*

----

* **Test JPP_0350**

  [VALUE_DETECTION / BADCASE]

   **JSON file with parameter of type 'list' / index (in square brackets) defined inside the curly brackets (invalid syntax 1)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 1 / pattern 1*

----

* **Test JPP_0351**

  [VALUE_DETECTION / BADCASE]

   **JSON file with parameter of type 'list' / index (in square brackets) defined inside the curly brackets (invalid syntax 2)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 1 / pattern 2*

----

* **Test JPP_0352**

  [VALUE_DETECTION / BADCASE]

   **JSON file with parameter of type 'list' / index (in square brackets) defined inside the curly brackets (invalid syntax 3)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 1 / pattern 3*

----

* **Test JPP_0353**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more opening elements '${' than closing elements '}' (invalid syntax 1)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 2 / pattern 1*

----

* **Test JPP_0354**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more opening elements '${' than closing elements '}' (invalid syntax 2)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 2 / pattern 2*

----

* **Test JPP_0355**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more opening elements '${' than closing elements '}' (invalid syntax 3)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 2 / pattern 3*

----

* **Test JPP_0356**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more opening elements '${' than closing elements '}' (invalid syntax 4)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 2 / pattern 4*

----

* **Test JPP_0357**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more opening elements '${' than closing elements '}' (invalid syntax 5)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 2 / pattern 5*

----

* **Test JPP_0358**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more opening elements '${' than closing elements '}' (invalid syntax 6)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 2 / pattern 6*

----

* **Test JPP_0359**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more opening elements '${' than closing elements '}' (invalid syntax 6)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 2 / pattern 7*

----

* **Test JPP_0360**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more opening elements '${' than closing elements '}' (invalid syntax 9)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 2 / pattern 8*

----

* **Test JPP_0361**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more closing elements '}' than opening elements '${' (invalid syntax 1)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 3 / pattern 1*

----

* **Test JPP_0362**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more closing elements '}' than opening elements '${' (invalid syntax 2)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 3 / pattern 2*

----

* **Test JPP_0363**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more closing elements '}' than opening elements '${' (invalid syntax 3)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 3 / pattern 3*

----

* **Test JPP_0364**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more closing elements '}' than opening elements '${' (invalid syntax 4)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 3 / pattern 4*

----

* **Test JPP_0365**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more closing elements '}' than opening elements '${' (invalid syntax 5)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 3 / pattern 5*

----

* **Test JPP_0366**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression containing more closing elements '}' than opening elements '${' (invalid syntax 6)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 3 / pattern 6*

----

* **Test JPP_0367**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression starting with '${' and ending with '}', further matching '${' and '}' in between (not all nested) (invalid syntax 1)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 6 / pattern 1*

----

* **Test JPP_0368**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression starting with '${' and ending with '}', further matching '${' and '}' in between (not all nested) (invalid syntax 2)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 6 / pattern 2*

----

* **Test JPP_0369**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression starting with '${' and ending with '}', further matching '${' and '}' in between (not all nested) (invalid syntax 3)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 6 / pattern 3*

----

* **Test JPP_0370**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression starting with '${' and ending with '}', further matching '${' and '}' in between (not all nested) (invalid syntax 4)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 6 / pattern 4*

----

* **Test JPP_0371**

  [VALUE_DETECTION / BADCASE]

   **JSON file with expression starting with '${' and ending with '}', further matching '${' and '}' in between (not all nested) (invalid syntax 5)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Checklist rule 6 / pattern 5*

----

* **Test JPP_0500**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file with composite data structure (nested lists and dictionaries 1)**

   Expected: JsonPreprocessor returns expected value

   *Hint: Standard notation*

----

* **Test JPP_0501**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file with composite data structure (nested lists and dictionaries 2)**

   Expected: JsonPreprocessor returns expected value

   *Hint: Dotdict notation*

----

* **Test JPP_0502**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file with composite data structure (nested lists and dictionaries 3 / some key names with dots inside)**

   Expected: JsonPreprocessor returns expected value

   *Hint: Standard notation*

----

* **Test JPP_0503**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file with composite data structure (some lists)**

   Expected: JsonPreprocessor returns expected value

----

* **Test JPP_0505**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file with composite strings containing several times a colon and a comma (JSON syntax elements)**

   Expected: JsonPreprocessor returns expected value

----

* **Test JPP_0506**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file with composite strings containing several combinations of curly brackets and special characters before**

   Expected: JsonPreprocessor returns expected value

----

* **Test JPP_0507**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file containing several string concatenations in separate lines (1)**

   Expected: JsonPreprocessor returns expected value

----

* **Test JPP_0508**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file containing several string concatenations in separate lines (2)**

   Expected: JsonPreprocessor returns expected value

----

* **Test JPP_0509**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file containing several parameter assignments in separate lines (different syntax)**

   Expected: JsonPreprocessor returns expected value

----

* **Test JPP_0510**

  [COMPOSITE_EXPRESSIONS / GOODCASE]

   **JSON file containing several parameter assignments in separate lines (extended string concatenation)**

   Expected: JsonPreprocessor returns expected value

----

* **Test JPP_0550**

  [COMPOSITE_EXPRESSIONS / BADCASE]

   **JSON file with composite data structure (nested lists and dictionaries / some key names with dots inside)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

   *Hint: Dotdict notation (ambiguous in this case)*

----

* **Test JPP_0600**

  [CODE_COMMENTS / GOODCASE]

   **JSON file with several combinations of code comments**

   Expected: JsonPreprocessor returns remaining content of JSON file (valid parameters)

----

* **Test JPP_0950**

  [COMMON_SYNTAX_VIOLATIONS / BADCASE]

   **JSON file with syntax error (1)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0951**

  [COMMON_SYNTAX_VIOLATIONS / BADCASE]

   **JSON file with syntax error (2)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0952**

  [COMMON_SYNTAX_VIOLATIONS / BADCASE]

   **JSON file with syntax error (3)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0953**

  [COMMON_SYNTAX_VIOLATIONS / BADCASE]

   **JSON file with syntax error (4): file is completely empty**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_0954**

  [COMMON_SYNTAX_VIOLATIONS / BADCASE]

   **JSON file with syntax error (5): file is empty (multiple pairs of brackets only)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_1000**

  [IMPLICIT_CREATION / GOODCASE]

   **JSON file with dictionary keys to be created implicitly**

   Expected: JsonPreprocessor returns values

----

* **Test JPP_1001**

  [IMPLICIT_CREATION / GOODCASE]

   **JSON file with dictionary keys to be created implicitly (same key names at all levels)**

   Expected: JsonPreprocessor returns values

----

* **Test JPP_1150**

  [CYCLIC_IMPORTS / BADCASE]

   **JSON file with cyclic imports (JSON file imports itself)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_1151**

  [CYCLIC_IMPORTS / BADCASE]

   **JSON file with cyclic imports (JSON file imports another file, that is already imported)**

   Expected: No values are returned, and JsonPreprocessor throws an exception

----

* **Test JPP_1200**

  [PATH_FORMATS / GOODCASE]

   **Relative path to JSON file**

   Expected: JsonPreprocessor resolves the relative path and returns values from JSON file

   *Hint: Works with raw path to JSON file (path not normalized internally)*

----

Generated: 20.11.2023 - 15:42:16

