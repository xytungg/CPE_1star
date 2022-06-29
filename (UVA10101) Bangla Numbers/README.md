# (UVA10101) Bangla Numbers  2022/06/29
>Tips：陣列
Q：kuti(10000000)、lakh(100000)、hajar(1000)、shata(100)
Eg：23764000，會輸出2 kuti 37 lakh 64 hajar0
```c++
#include <stdio.h>
void bangla(long long n){
	if(n >= 10000000){
		bangla(n/10000000);
		printf(" kuti");
		n=n%10000000;
	}
	if(n >= 100000){
		printf(" %lld lakh", n/100000);
		n=n%100000;
	}
	if(n >= 1000){
		printf(" %lld hajar", n/1000);
		n=n%1000;
	}
	if(n >= 100){
		printf(" %lld shata", n/100);
		n=n%100;
	}
	if(n!=0){
		printf(" %lld", n);
	}
}
int main()
{
	long long n, c=1;
	while(scanf("%lld", &n)==1){
		printf("%4lld.", c++);
		if(n!=0) bangla(n);
		else printf(" 0");
		printf("\n");
	}
}
```
