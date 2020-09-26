# os-Linux
## Ex.1_1
### hello.c
```C
#include<stdio.h>
#include<stdlib.h>

int main()
{
	printf("Hello World\n");
	exit(0);
}
```
### bush
<img width="358" alt="screenshot 1 1" src="https://user-images.githubusercontent.com/63101910/93661784-3ff5c880-fa63-11ea-877a-b9f7fa990676.PNG">

## Ex.1_2
### fred.c
```C
#include <stdio.h>

void fred(int arg) {
    printf("fred: you passed %d\n", arg);
}
```

### bill.c
```C
#include <stdio.h>

void bill(char* arg) {
    printf("bill: you passed %s\n", arg);
}
```
### bush
gcc -c fred.c bill.c

ls *.o

### output
![image](https://user-images.githubusercontent.com/63101910/93662952-b0551780-fa6c-11ea-9180-11a2a875dc5d.png)

### lib.h
```C
void bill(char*);
void fred(int);
```
### program.c
```C
#include <stdio.h>
#include <stdlib.h>
#include "lib.h"

int main() {
    bill("Hello world");
    exit(0);
}
```
### bush
![image](https://user-images.githubusercontent.com/63101910/93663017-3e310280-fa6d-11ea-99cd-acad9d88e382.png)

## Ex.1_3
### bush
man gcc

### output
![image](https://user-images.githubusercontent.com/63101910/93664573-9faa9e80-fa78-11ea-98b3-2809b251d9ef.png)

## Ex.2_1
### 2_1.sh
```C
#!/bin/sh
myvar="Hi there"
echo $myvar
echo "$myvar"
echo '$myvar'
echo \$myvar

echo Enter some text
read myvar

echo '$myvar' now equals $myvar
exit 0
```
### bush 
![image](https://user-images.githubusercontent.com/63101910/94337392-b90c9700-fff2-11ea-8960-91635840d1b9.png)

## Ex.2_2
### 2_2.sh
```C
#!/bin/sh

salutation="Hello"
echo $salutation
echo "The program $0 is now running"
echo "The second parameter was $2"
echo "The first parameter was $1"
echo "The parameter list was $*"
echo "The user's home directory is $HOME"
echo "Please enter a new greeting"
read salutation

echo $salutation
echo "The script is now complete"
exit 0
```
### bush
![image](https://user-images.githubusercontent.com/63101910/94337726-78624d00-fff5-11ea-9fe1-c102cec27037.png)

## Ex.2_3
### 2_3.sh
```C
echo "Is it morning? yes or no "
read timeofday

if [ "$timeofday" = "yes" ]
then
   echo "Good morning"
elif [ "$timeofday" = "no" ]; then
  echo "Good afternoon"
else
  echo "Sorry, $timeofday not recognized"
exit 1
fi
exit 0
```
### bush
![image](https://user-images.githubusercontent.com/63101910/94338420-b31ab400-fffa-11ea-8684-1c14f427b7cc.png)

## Ex.2_4
### 2_4.sh
```C
#!/bin/sh

for foo in bar fud 43
do
  echo $foo
done
exit 0
```
### bush
![image](https://user-images.githubusercontent.com/63101910/94338675-d6466300-fffc-11ea-9053-bcc767ff8faf.png)








