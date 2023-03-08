# Notes for bash

## string split
* remove prefix: `cell=${MYFILE#.sorted.bam}`
* remove suffix: `cell=${MYFILE%.sorted.bam}`
* remove suffix (alternative way) and keep basename:
  `NAME=$(basename /foo/fizzbuzz.bar .bar)`
  
* `cut`: split string with delimiter: `echo "my file is here" | cut -d " " -f 2`
* `awk`: similarly `echo "my file is here" | awk -F " " '{print $2}'`
* `tr` : split string into array `my_array=$(echo "my file is here" | tr " " "\n")`




## parallel computing

https://medium.com/@robert.i.sandor/getting-started-with-parallelization-in-bash-e114f4353691

```bash
N=4
for thing in a b c d e f g; 
do 
   ((i=i%N)); ((i++==0)) && wait
   echo "$thing" &
done
```
## parse tsv or csv file

```bash
while IFS=$',' read -r -a myArray
do
    echo "${myArray[0]}"
    echo "${myArray[1]}"
done < my_file
```


## grep multiple patterns

```bash
grep "Unique\|mapped length\|Mismatch" */NC_007605.1.STAR.bulkLog.final.out
```

## view folder structure

```bash
tree -L 2
```

## FTP download

```
wget --mirror --user=YOUR_USER --ask-password ftp://YOURSITE/YOUR_FOLDER[*]
```

