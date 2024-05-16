## Syntax-Analysis

### Overview

- Can construct and display LR(0) DFA and LR(1) DFA
- Can judge the grammer
- Can construct LR(0)/SLR(1)/LR(1)/LALR(1) ACTION/GOTO tables
- Can judge whether the sentence is generated by the given grammar

### Requirements

- Python 3
- python-graphviz (optional)
  - Users can install it by running `pip install graphviz`

### DFA Sample Generation

#### LR(0) DFA

- Sample LR(0) grammer
    ```bash
    E->E+T|T
    T->(E)|d
    # should not have new line at the end of the file
    ```
- Sample-generated DFA: <br>
![sample LR(0) DFA](img/sample_LR(0)_dfa.png)

#### LR(1) DFA

- Sample LR(1) grammer
    ```
    E->(L,E)|F
    L->L,E|E
    F->(F)|d
    ```
- Sample-generated DFA: <br>
![sample LR(1) DFA](img/sample_LR(1)_dfa.png)

### Simple Calculator

File folder `calculator` contains a python calculator based on LR parsing.