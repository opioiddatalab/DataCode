# PubMed search volume results

## Description
If you want to see how many PubMed query results there are for each of these terms, you can use this Python code, filling in you [API key](https://ncbiinsights.ncbi.nlm.nih.gov/2017/11/02/new-api-keys-for-the-e-utilities/).

## Required Input
Input is a CSV with a single column (no header row) listing each search term on a separate line. 

## Metadata
Language: Python 3.7<br>
Published: December 1, 2019
<br>

```python
import operator
import pandas as pd
from Bio import Entrez

df = pd.read_csv('searchdrug.csv', header=0)
df.head()

# create output dictionary
outputdict={}

df['count']=pd.Series()
for i, row in df.iterrows():
    Entrez.email = "email@domain.com"
    handle = Entrez.esearch(db="pubmed", term=row['brand'], retmode="xml", datetype="pdat", api_key="INSERT PRIVATE API KEY HERE ")
    records = Entrez.read(handle)
    brand = row['brand']
    count = int(records["Count"])
    # populate output dictionary
    outputdict[brand] = str(count)

# generate sorted list from outputdict
for b,c in sorted(outputdict.items(), key=operator.itemgetter(1), reverse=True):
    print(b,c)

# convert to dataframe    
list=pd.DataFrame.from_dict(outputdict,orient='index')

list.to_csv('freqlist.csv', header=0)
```

## MIT License
Copyright 2019 Opioid Data Lab

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
