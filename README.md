# shell_one-liners

Single lines of bash commands 

## Contents

- [find & grep](#find--grep)

Read lines, search for string in each line, and find matching files with '.ab1' extension

    while read line; do find . -type f -name "*.ab1" -exec grep -l "$line" /dev/null '{}' \+; done < ../voucher_id_list.txt
    while read line; do grep -l -r "$line" .; done < ../voucher_id_list.txt
    grep -l -f ../voucher_id_list.txt ./*
    
Read list and move files  

    while IFS= read -r file; do mv "$file" /destination_folder/; done < list.txt
    for i in $(cat list.txt); do mv "$i" /destination_folder/; done
    
Compare files line by line 

    diff file1 file 2
    # Output: %< lines from file1, %> lines from file2, %= lines common to file1 and file2
  
