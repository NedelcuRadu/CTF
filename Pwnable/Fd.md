# Fd
> SSH Info: ssh fd@pwnable.kr -p2222  
> Password: guest

## Hint
>Mommy! what is a file descriptor in Linux?

## Code
```cpp
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
char buf[32];
int main(int argc, char* argv[], char* envp[]){
	if(argc<2){
		printf("pass argv[1] a number\n");
		return 0;
	}
	int fd = atoi( argv[1] ) - 0x1234;
	int len = 0;
	len = read(fd, buf, 32);
	if(!strcmp("LETMEWIN\n", buf)){
		printf("good job :)\n");
		system("/bin/cat flag");
		exit(0);
	}
	printf("learn about Linux file IO\n");
	return 0;

}

```
We need to get buf equal to `LETMEWIN`, but how we do that? We need to exploit the [`read`](http://codewiki.wikidot.com/c:system-calls:read) function in order to make it read from stdin, that means setting fd to 0.


**Password:** boJ9jbbUNNfktd78OOpsqOltutMc3MY1


[Next Level](../Bandit%201%20--%202/README.md)
