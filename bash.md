# Notes for bash

## string split

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