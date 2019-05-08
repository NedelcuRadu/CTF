# Random
> SSH Info: ssh random@pwnable.kr -p2222   
> Password: guest

## Hint
>Daddy, teach me how to use random value in programming!

## Code
```cpp
#include <stdio.h>

int main(){
	unsigned int random;
	random = rand();	// random value!

	unsigned int key=0;
	scanf("%d", &key);

	if( (key ^ random) == 0xdeadbeef ){
		printf("Good!\n");
		system("/bin/cat flag");
		return 0;
	}

	printf("Wrong, maybe you should try 2^32 cases.\n");
	return 0;
}
```
We have to find a value that XOR'd with random results in `0xdeadbeef`. We notice that the rand() function doesn't have a seed, so its value will be constant.
Following code will find the key:
```cpp
#include <stdio.h>
int main(){
	unsigned int random;
	random = rand();	// random value!
  int beef= 0xdeadbeef;
  printf("%d", beef ^ random);
	return 0;
}
```
As expected, when we enter it we get our flag:
```
random@ubuntu:~$ ./random
-1255736440
Good!
Mommy, I thought libc random is unpredictable...
```
**Flag:** Mommy, I thought libc random is unpredictable...


[Next Level]()
