# (UVA100) The 3n + 1 problem 2022/06/28
>Tips：陣列
Q：如果是奇數：乘3+1  ，如果是偶數：除以2  
Eg：n=10，10-5-16-8-4-2-1，長度為7，計算得到1之前計算幾回？

```c++
#include <iostream>
using namespace std;
int main()
{
	int a, b;
	while(cin>>a>>b){
		cout<<a<<" "<<b<<" ";
		if(a>b){int c=a; a=b; b=c; }
		int maxLen=0;
		for(int i=a; i<=b; i++){
			int n=i, len=1;
			while(true){
				if(n==1) break;
				if(n%2!=0) n=n*3+1;
				else n/=2;
				len++;
			}
			maxLen=max(len, maxLen);
		}
		cout<< maxLen <<endl;
	}

}
```
