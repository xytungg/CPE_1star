# (UVA10008) What's Cryptanalysis?   2022/07/05
>tips：字串、記數  
Q：統計英文字母出現次數，依照次數大到小排列，若次數相同則先印排列較前的字母
```c
#include <iostream>
#include <cctype>
using namespace std;
int count[256];
int l;

int main(){
	char c;
	while(cin>>c)
	l++,count[toupper(c)]++;
	while(--l){
		for(c='A';c<='Z';c++){
			if(count[c]==l)
			cout<<c<<" "<<count[c]<<endl;
		}
	}
}
```
