# Wrangling text data

## Play:
1. I was assigned to take play related to "The Tempest" as per the number assigned for me in the [big data developers](https://github.com/denisecase/big-data-developers).  
2. My speaker 1 is "Master".
3. My speaker 2 is "Boatswain"
4. Below are the commands used for generating data and results file using Bash.

## Bash 

Fetching with Bash.

```Bash
curl "http://shakespeare.mit.edu/tempest/full.html" | sed 's/<\/*[^>]*>//g' > tempest.txt
```

Finding matches with Bash.

```Bash
grep 'Master' tempest.txt
grep 'Boatswain' tempest.txt
grep -i 'Boatswain' tempest.txt -c
grep -i 'Master' tempest.txt -c

cat tempest.txt | grep -i 'master' -c

grep -i '^Boatswain$' tempest.txt -c
grep -i '^master$' tempest.txt -c

```

Processing text with Bash (sorting, counting)

```Bash
tr ' ' '\12' < tempest.txt | sort | uniq -c | sort -nr > tempresult.txt
```

Previewing content with Bash (cat, head, tail)

```Bash
cat tempresult.txt
head -10 tempresult.txt
tail -4 tempresult.txt 
```
## What is Data Wrangling?  
Data wrangling is the process of cleaning, structuring and enriching raw data into a desired format for better decision making in less time. Data wrangling is increasingly ubiquitous at today’s top firms. Data has become more diverse and unstructured, demanding increased time spent culling, cleaning, and organizing data ahead of broader analysis. At the same time, with data informing just about every business decision, business users have less time to wait on technical resources for prepared data.  

This necessitates a self-service model, and a move away from IT-led data preparation, to a more democratized model of self-service data preparation or data wrangling. This self-service model with data wrangling tools allows analysts to tackle more complex data more quickly, produce more accurate results, and make better decisions. Because of this ability, more businesses have started using data wrangling tools to prepare before analysis.  
