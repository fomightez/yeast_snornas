# yeast_snornas
**scripts and files for accounting for yeast snoRNAs among a gene list**


---



**Description of each script and file**



- `????.py`

>  lists --> list of shared items and a diagram showing relationships between lists  
Like `find_overlap_in_lists.py` (see below), except for in the cases of comparisons involving 2 or 3 list documents, it produces an area-weighted Venn diagram (image file) depicting the relationships of the items in the lists. 
For comparing 4 lists, a Venn diagram will also be generated but it will not be area-wighted. To produce a Venn diagram for comparing lists found in four separate documents, it requires `venn4_from_github.py` (see below) in the same directory. This additional script is not needed in the cases comparing two or three lists.  
Note: The core of this script and related code can produce a Venn diagram on [mybinder.org](http://mybinder.org)-derived Binders if  `%matplotlib notebook` or `%matplotlib inline` is invoked as the first line, see [this demo](https://gist.github.com/fomightez/5575a91be88955257ba1f658ff253197).  
See `find_overlap_in_lists.py` below for additional details.

**Usage**  

```
usage:  

```

**example of input and output for `????.py`:**

**original input:**  
(text ????)
```

                            






```

**command:**

    ???????

**output after run:**  
(text in a file, called `????` , with the contents below)
```
""""""


```
 

---

- `????.tsv`

>  Tab-delimited table derived from the Founier Lab's Yeast snoRNA database. The table is presently at ????? but it will soon the site will migrate. Already the site is hard to access, and because of that the script doesn't feature a way to retrieve the data via the web. Instead, this already script-useable table is provided for use with the script. You'll need to insure it is the same directory as the script.

---


Related scripts
---------------

Since this repository concerns using annotations, data mining, and text manipulations, processes which are at the heart of most of my computational endeavors, the repository overlaps with themes present in other repositories. Here are some related oes:

- [My sequence work repository](https://github.com/fomightez/sequencework) has code for adjusting annotations and gene lists

- [My text mining repository](https://github.com/fomightez/text_mining) has code for dealing with lists in general
