
3.1. Есть такие данные в одну строку:

{"count": 36, "next": ..........

Нужно вывести все двузначные числа, которые стоят в кавычках.

Решение:

cat simple.txt | grep -oE '"[0-9]{2}"'


3.2. Есть папки:

20160118//  20160208// .......

Написать как запаковать в tar.gz все папки, начинающиеся с 2016 или содержащие в начале имени 4 цифры и удалить их после запаковки.

Решение:

tar -czvf arch.tar.gz [0-9][0-9][0-9][0-9]* |  while read I ; do  rmdir   "$I" ; done
