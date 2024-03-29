# Implementing Merkle Tree in Python

[//]: # (Image References)

[treeImage]: ./tree_structure.png "Hash Tree Structure"

## Merkle Tree coding challenge
[Requirements Details](https://geod24.github.io/infrastructure/)


## Getting Started
These instructions will get you a copy of the project up and running on your local machine for testing purpose. 

### Python version
It runs on any version of Python 2.7 or newer. Mac OS X or Linux comes with Python 2.7 out of the box.

### Getting source files from the github
Open Terminal and get the source files

```
git clone https://github.com/linked0/merkle-tree.git
```
### Running the script
Go to merkle-tree/python directory and run Python script.
```
cd merkle-tree/python
python merkle.py "The quick brown fox" "jump over" "the" "lazy dog"
```
You can get the result as follows.
```
Level 0:
018FB04252A594A8049CBFE9E34848249040E1FA7E170501E17ADC06393D4DC3
Level 1:
836C2FE675884DB41C49215F8A91E6560B1EA752F683DB793E9B86180CA235F8
49B9A6B1346DC768898A16C2DAD9D554349C9150F8B2809AC7D48B305C4D3650
Level 2:
7743034D22491720B723B68AFD046BE66969409254DC79A153E290C81A8F238A
F51DF418D9D7BAFDCFDC4320409E08E39858D0D686FEE959EA545E6D7C214F71
1E7C521A055F0F08CEA3FADED5923CCA2D8F4366A62AAA8A8B843A842AA656B8
144BEE93D8F6350C6E38C96EEB11DE2CD249A7BD5D23FF4C91EB46573B5AF3BA
```

## Jupyter notebook in Google Colabotory(Colab.) environment(Optional)
Using the Jupyter notebooks is the easiest way to run the python code.
If you have a google account, you can run my Python implementation in the Google Colab. Please follow steps below.

1. Click on the link:
[Jay's implementation of Merkle tree in Google Colab.](https://colab.research.google.com/github/linked0/merkle-root/blob/master/python/merkle_tree.ipynb)
2. Google sign-in required
3. Select "CONNECT" at the top-right of the menu bar.
4. Click each cell and press Ctrl+Enter to run the code.
5. If you have the pop-up showing the message such as "Warning: This notebook was not authored by Google.", just select "RUN ANYWAY" at the bottom-right of the pop-up.
6. If you have the pop-up showing the message such as "Reset all runtimes", just select "YES" at the bottom-right of the pop-up.

## Implemtation details
### MerkleTree class
#### Member variables

| Name | Description|
| :--- | :--- |
| leaf_data | It is a list which contains the original input data such as "The quick brown fox" or "jump over". |
| root_node | It is the root node of a Merkle tree that contains child nodes. Each node is implemented with the Map data structure. (Dictionary type in Python) |

#### Member functions
| Name | Description|
| :--- | :--- |
| make_tree | It makes a balanced hash tree with each node storing the hash value computed by a hash function |
| get_double_sha256 | It has the input parameter double-sha256 hashed |
| print_tree | It prints the hash value from top to leaf nodes |
| convert_binary_to_ascii | It converts a binary string to a ascii string.|

### Data structure and implementation in Python
![alt text][treeImage]