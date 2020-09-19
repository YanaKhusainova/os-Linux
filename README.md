# os-Linux
## Ex.1
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

## Ex.2
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
gcc -o fred.c bill.c
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









