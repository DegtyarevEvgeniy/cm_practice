# Практическое занятие №1. Введение, основы работы в командной строке


## Задача 1
```cut -d: -f1 /etc/passwd |sort```

![pic/1.png](pic/1.png)

## Задача 2
```awk '{print $2, $1}' /etc/protocols | sort -k1,1nr | head -n 5```

![pic/2.png](pic/2.png)

## Задача 3
```
#!/bin/bash

if [ $# -eq 0 ]; then
    echo "Использование: $0 \"Ваш текст\""
    exit 1
fi

text="$1"

length=${#text}

border=$(printf "%0.s-" $(seq 1 $((length + 2))))

border="+$border+"

echo "$border"
echo "| $text |"
echo "$border"
```            

![pic/3.png](pic/3.png)

## Задача 4
```
grep -oE '\b[a-zA-Z_][a-zA-Z0-9_]*\b' test.c | grep -vE '\b(int|void|return|if|else|for|while|include|stdio)\b' | sort | uniq
```

![pic/4.png](pic/4.png)

## Задача 5
```
chmod +x reg
sudo cp $1 /usr/local/bin
```

![pic/5.png](pic/5.png)


## Задача 6
```
chmod +x check_comment.sh
./check_comment.sh
```

![pic/6.png](pic/6.png)


## Задача 7
```
chmod +x find_duplicates.sh
./find_duplicates.sh /Users/aslav/Documents/cdr
```

![pic/7.png](pic/7.png)


## Задача 8
```
go run archiver.go /Users/aslav/Documents/cdr  .log
```

![pic/8.png](pic/8.png)

## Задача 9
```
cd code
go run replacer.go /Users/aslav/Desktop/RTU_MIREA_2COURCE/КонфигУправ/1Pract/trash/testFor8.txt testFor8output.txt

```

![9questTerminal.png](pic/9.png)
![9questFile.png](pic/91.png)

## Задача 10
```
cd code
go run dirReader.go /Users/aslav/Downloads 
```

![pic/10.png](pic/10.png)
