# yeast_snornas
**scripts and files for accounting for yeast snoRNAs among a gene list**


---



**Description of each script and file**



- `delineate_properties_of_yeast_snoRNAs_in_gene_list.py`

>  list of genes --> thorough accounting of the snoRNAs in that list    
`delineate_properties_of_yeast_snoRNAs_in_gene_list.py` takes a gene list and looks for all the snoRNAs it contains. snoRNAs fall into several categories based on family, target, etc. and an account of those falling in these various categories is generated. The output will include an analysis of enrichment for each of the categories of yeast snoRNAs.  
The script relies on a tab-separated values table that is provided in the repository with the script.  
You will also need to provide a gene list in the same repository as the script. See details below.

**Usage**  

```
usage:  

```

**Preparation**

As of now, some user-adjustable variables have to be adjusted within the text of the code for the script to run. Specifically, you have to change the variable `gene_list_file_name` to have the value of your gene list file. For example, let's say your file was named "NOISeq_upregulated_gene_list.txt", the line involving `gene_list_file_name` (currently around line 130) would need to be edited to be:
```
gene_list_file_name = "NOISeq_upregulated_gene_list.txt"
```
Place your gene list file in the same directory as the tab-separated values table and the script. DESCRIBE GENE LIST NEEDS HERE!!!!


**example of input and output for `delineate_properties_of_yeast_snoRNAs_in_gene_list.py`:**

**original input:**  
(text produced will be saved as ????)
```

                            






```

**command:**
```
python delineate_properties_of_yeast_snoRNAs_in_gene_list.py
```

**output after run:**  
(text in a file, called `????` , with the contents below)
```
""""""


```
 

---

- `raw_yeast_snoRNA_table_as_tsv.txt`

>  The file is a dab-delimited table version of a table of yeast snoRNA information and characteristics presently from Founier Lab's Yeast snoRNA database, specifically http://people.biochem.umass.edu/sfournier/fournierlab/snornadb/mastertable.php . It is provided here as `raw_yeast_snoRNA_table_as_tsv.txt` along with the script `delineate_properties_of_yeast_snoRNAs_in_gene_list.py`.  
The table is presently part of the Founier Lab's Yeast snoRNA database hosted on the UMass Amherst biochemistry department site, but the site will soon move. Already the site where the table resides can be hard to access as it undergoes bit-rot, and because of that the script purposefully doesn't feature a way to retrieve the data via the web. Instead, this already script-useable table is provided for use with the script. You'll need to insure it is the same directory as the script.

---


Related scripts
---------------

Since this repository concerns using annotations, data mining, and text manipulations, processes which are at the heart of most of my computational endeavors, the repository overlaps with themes present in other repositories. Here are some related oes:

- [My sequence work repository](https://github.com/fomightez/sequencework) has code for adjusting annotations and gene lists

- [My text mining repository](https://github.com/fomightez/text_mining) has code for dealing with lists in general
