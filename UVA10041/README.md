# (UVA10041) Vito'sfamily 2022/06/27
```c++
#include <iostream>
#include <algorithm>
#include <vector>
using namespace std;
vector<int> num;

int main()
{
	int n, parent, street;
	cin>>n;
	while(n--){
		cin>>parent;
		num.clear();
		for(int i=0; i<parent; i++){
			cin>>street;
			num.push_back(street);
		}
		
		sort(num.begin(), num.end());
		int mid=num[parent/2];
		int sum=0;
		for(int i=0; i<parent; i++){
			sum+=abs(num[i]-mid);
		}
		cout<<sum<<endl;
	}
}
```
