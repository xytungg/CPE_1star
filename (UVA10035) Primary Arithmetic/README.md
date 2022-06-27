# (UVA10035) Primary Arithmetic  2022/06/27
>Q：計算進位次數
```c
#include <stdio.h>
int main()
{
	int a, b;
	while(scanf("%d%d", &a, &b)==2){
		if(a==0 && b==0) break;
		int carry=0, ans=0;
		while(a>0 || b>0){
			int aa=a%10, bb=b%10;
			if(aa+bb+carry>=10){
				carry=1;
				ans++;
			}else{
				carry=0;
			}
			a=a/10;
			b=b/10;			
		}
		if(ans==0) printf("No carry operation.\n");
		else if(ans==1) printf("1 carry operation.\n");
		else printf("%d carry operations.\n", ans);
	}
}
```
