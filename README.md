# yeast_snornas
**scripts and files for accounting for yeast snoRNAs among a gene list**


---



**Description of each script and file**



- `delineate_properties_of_yeast_snoRNAs_in_gene_list.py`

>  list of genes --> thorough accounting of the snoRNAs in that list    
`delineate_properties_of_yeast_snoRNAs_in_gene_list.py` takes a gene list and looks for all the snoRNAs it contains. Such a list may come from an RNA-Seq or microarray analysis or other type of high-throughput genetics experment. snoRNAs fall into several categories based on family, target, etc. and an account of those falling in these various categories is generated. The output will include an analysis of enrichment for each of the categories of yeast snoRNAs.  
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
**Example standard out buffer streamed to command line console:**
```
15:28 ~/scripts/snoRNA_pandas$ python delineate_properties_of_yeast_snoRNAs_in_gene_list.py
Data on 77 snoRNAs read in from 'raw_yeast_snoRNA_table_as_tsv.txt'.
Reading gene list file...

618 genes listed in 'downregulated.txt'; 50, or 8.09%, of those genes are snoRNAs.
By comparison, the 77 snoRNAs recognized in the yeast genome are 1.10% of all 6993 recognized genes in the yeast genome.
The set of snoRNAs contained in the provided gene list represents 64.94% of all yeast snoRNAs.
This represents a 7.35 fold-enrichment over the expected (p-value = 1.47E-34 in support of over-representation by one-tailed Fisher's Exact Test).

Concerning H/ACA snoRNAs:
The provided gene list contains 22 such snoRNAs.
Those are: [snR11, snR10, snR3, snR9, snR8, snR82, snR83, snR81, snR86, snR84, snR85, snR161, snR189, snR46, snR42, snR43, snR49, snR36, snR33, snR32, snR30, snR191]
This represents 75.86 % of the 29 H/ACA snoRNAs
This represents a 8.58 fold-enrichment over the expected (p-value = 4.01E-18 in support of over-representation by one-tailed Fisher's Exact Test).

Concerning MRP snoRNAs:
The provided gene list contains 1 such snoRNAs.
Those are: [NME1]
This represents 100.00 % of the 1 MRP snoRNAs

Concerning C/D snoRNAs:
The provided gene list contains 27 such snoRNAs.
Those are: [snR55, snR54, snR57, snR56, snR51, snR50, snR17a, snR52, snR79, snR78, snR71, snR4, snR17b, snR87, snR73, snR45, snR68, snR69, snR40, snR65, snR67, snR60, snR61, snR62, snR63, snR76, snR39B]
This represents 57.45 % of the 47 C/D snoRNAs

Concerning Monocistronic snoRNAs:
The provided gene list contains 40 such snoRNAs.
Those are: [snR71, snR56, snR50, snR17a, snR52, snR11, snR10, snR79, snR3, snR4, snR9, snR8, snR17b, snR82, snR83, snR81, snR86, snR87, snR84, snR85, snR161, snR43, snR189, snR68, snR32, snR46, snR45, snR42, snR69, snR40, snR65, snR60, snR62, snR49, snR63, NME1, snR36, snR33, snR39B, snR30]
This represents 76.92 % of the 52 Monocistronic snoRNAs
This represents a 8.70 fold-enrichment over the expected (p-value = 1.64E-32 in support of over-representation by one-tailed Fisher's Exact Test).

Concerning Intronic snoRNAs:
The provided gene list contains 2 such snoRNAs.
Those are: [snR191, snR54]
This represents 25.00 % of the 8 Intronic snoRNAs

Concerning Polycistronic snoRNAs:
The provided gene list contains 8 such snoRNAs.
Those are: [snR55, snR73, snR57, snR78, snR51, snR76, snR67, snR61]
This represents 47.06 % of the 17 Polycistronic snoRNAs

Concerning pol II-transcribed snoRNAs:
The provided gene list contains 49 such snoRNAs.
Those are: [snR55, snR54, snR71, snR56, snR51, snR50, snR17a, snR11, snR10, snR79, snR78, snR57, snR3, snR4, snR9, snR8, snR17b, snR82, snR83, snR81, snR86, snR87, snR84, snR85, snR161, snR73, snR43, snR189, snR68, snR32, snR46, snR45, snR42, snR69, snR40, snR65, snR67, snR60, snR61, snR62, snR49, snR63, snR76, NME1, snR36, snR33, snR39B, snR30, snR191]
This represents 64.47 % of the 76 pol II-transcribed snoRNAs
This represents a 7.30 fold-enrichment over the expected (p-value = 1.16E-33 in support of over-representation by one-tailed Fisher's Exact Test).

Concerning pol III-transcribed snoRNAs:
The provided gene list contains 1 such snoRNAs.
Those are: [snR52]
This represents 100.00 % of the 1 pol III-transcribed snoRNAs

Concerning guide element-possessing H/ACA snoRNAs:
The provided gene list contains 21 such snoRNAs.
Those are: [snR82, snR83, snR81, snR86, snR43, snR84, snR85, snR11, snR10, snR33, snR49, snR191, snR36, snR3, snR189, snR42, snR32, snR161, snR9, snR8, snR46]
This represents 75.00 % of the 28 guide element-possessing H/ACA snoRNAs
This represents a 8.49 fold-enrichment over the expected (p-value = 3.55E-17 in support of over-representation by one-tailed Fisher's Exact Test).

Concerning guide element-possessing C/D snoRNAs:
The provided gene list contains 25 such snoRNAs.
Those are: [snR55, snR54, snR57, snR56, snR51, snR50, snR17a, snR52, snR79, snR78, snR71, snR76, snR17b, snR87, snR73, snR68, snR69, snR40, snR65, snR67, snR60, snR61, snR62, snR63, snR39B]
This represents 55.56 % of the 45 guide element-possessing C/D snoRNAs

Concerning 18S-targeting snoRNAs:
The provided gene list contains 17 such snoRNAs.
Those are: [snR55, snR54, snR57, snR56, snR51, snR17b, snR17a, snR83, snR161, snR79, snR85, snR49, snR40, snR36, snR189, snR52, snR87]
This represents 60.71 % of the 28 18S-targeting snoRNAs

Concerning 18S-targeting H/ACA snoRNAs:
The provided gene list contains 6 such snoRNAs.
Those are: [snR83, snR85, snR161, snR49, snR36, snR189]
This represents 60.00 % of the 10 18S-targeting H/ACA snoRNAs

Concerning 18S-targeting C/D snoRNAs:
The provided gene list contains 11 such snoRNAs.
Those are: [snR55, snR54, snR57, snR56, snR51, snR17b, snR17a, snR52, snR79, snR40, snR87]
This represents 61.11 % of the 18 18S-targeting C/D snoRNAs

Concerning 25S-targeting snoRNAs:
The provided gene list contains 34 such snoRNAs.
Those are: [snR73, snR71, snR51, snR50, snR52, snR11, snR10, snR78, snR3, snR8, snR9, snR42, snR69, snR82, snR81, snR86, snR84, snR189, snR32, snR46, snR68, snR43, snR40, snR65, snR67, snR60, snR61, snR62, snR49, snR63, snR76, snR33, snR39B, snR191]
This represents 64.15 % of the 53 25S-targeting snoRNAs
This represents a 7.26 fold-enrichment over the expected (p-value = 1.52E-23 in support of over-representation by one-tailed Fisher's Exact Test).

Concerning 25S-targeting H/ACA snoRNAs:
The provided gene list contains 17 such snoRNAs.
Those are: [snR82, snR46, snR81, snR86, snR43, snR84, snR11, snR10, snR49, snR191, snR33, snR3, snR189, snR42, snR32, snR9, snR8]
This represents 77.27 % of the 22 25S-targeting H/ACA snoRNAs
This represents a 8.74 fold-enrichment over the expected (p-value = 1.72E-14 in support of over-representation by one-tailed Fisher's Exact Test).

Concerning 25S-targeting C/D snoRNAs:
The provided gene list contains 17 such snoRNAs.
Those are: [snR73, snR71, snR67, snR51, snR50, snR40, snR52, snR65, snR78, snR60, snR61, snR62, snR63, snR39B, snR69, snR68, snR76]
This represents 54.84 % of the 31 25S-targeting C/D snoRNAs

Concerning 5.8S-targeting snoRNAs:
The provided gene list contains 1 such snoRNAs.
Those are: [snR43]
This represents 100.00 % of the 1 5.8S-targeting snoRNAs

Concerning U2 snRNA-targeting snoRNAs:
The provided gene list contains 1 such snoRNAs.
Those are: [snR81]
This represents 100.00 % of the 1 U2 snRNA-targeting snoRNAs

Concerning orphan (no known guide element/pairing - directing interaction) snoRNAs:
The provided gene list contains 4 such snoRNAs.
Those are: [snR4, snR45, NME1, snR30]
This represents 100.00 % of the 4 orphan (no known guide element/pairing - directing interaction) snoRNAs
This represents a 11.32 fold-enrichment over the expected (p-value = 6.05E-05 in support of over-representation by one-tailed Fisher's Exact Test).
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

- [My YeastMine repository](https://github.com/fomightez/yeastmine) has a number of scripts for examining yeast genomic data and converting the output to different forms or useful data using YeastMine proromatically.
