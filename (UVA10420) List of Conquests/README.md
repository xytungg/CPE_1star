# (UVA10420) List of Conquests  2022/07/05
>tips：字串、排序  
Q：輸出每個國家的人數 依照國家名稱字母排序
```c
#include <iostream>
#include <map>
using namespace std;
int main(){
	int n;
	string country,people;
	map<string,int> a;
	map<string,int> ::iterator i;
	cin >> n;
	while(n--){
		cin >> country ;
		getline(cin , people);
		a[country]++;
	}
		for(i=a.begin();i!=a.end();i++){
			cout<< i->first << " " << i->second << endl;
		}
}
```
