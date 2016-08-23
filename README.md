# shell_one_liners

Single lines of bash commands 

## Contents

- [find & grep](#find--grep)

Read lines from file and use each line to find files with .ab1 extension

  while read voucher; do find . -type f -name "*.ab1" -exec grep -l "$voucher" /dev/null '{}' \+; done < ../voucher_id_list.txt
  
