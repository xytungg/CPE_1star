# (UVA10055) Hashmat the brave  2022/06/27
>Tips：整數 要使用long long  
Q：計算兩隊士兵差距

```c++
#include <iostream>
#include <cstdlib>
using namespace std;
int main()
{
	long long int a, b, ans=0;
	while(cin>>a>>b){
		cout<<abs(b-a)<<endl;
	}
}
```
