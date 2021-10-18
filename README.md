# UVA10041 Vito'sfamily 
### 題目 
https://onlinejudge.org/index.php?option=com_onlinejudge&Itemid=8&category=12&page=show_problem&problem=982
```c
#include <stdio.h>
#include <stdlib.h>
//提供給qsort使用的比較大小函數
//因為qsort的效果會將整個陣列，按由小而大的順序排列，所以：
//函數comp傳回>0時，表示a的資料大於b的資料，qsort會將a排在b的後面
//函數comp傳回<0時，表示a的資料小於b的資料，qsort會將a排在b的前面
//因為qsort在排序時，會對調元素的值，所以參數要用*間接定址才可以
int comp(const void *a, const void *b){
	return *(int *)a-*(int *)b;
}
int main(int argc, const char * argv[]){
	int s[500];
	int n, cs, i, k, median, sum;
	scanf("%d", &cs);	//讀入case個數
	for(int i=0; i<cs; i++){
		scanf("%d", &n);	//讀入成員人數，然後讀入每個成員居住的街道
		
		for(int k=0; k<n; k++)
			scanf("%d", &s[k]);
			
			//排序s陣列，有n項資料，每一個元素大小是sizeof(int)
			//同時，也告訴qsort排序時，兩項比大小的函數是comp
			qsort(s, n, sizeof(int), comp);
			median=s[n/2];	//找出中位數(住在最中間的成員)
			sum=0;	//計算每個成員與最中間成員的總和
			for(k=0; k<n; k++)
				sum+=abs(s[k]-median);
				
				printf("%d\n", sum);	//輸出距離總和

	}
		return 0;

}
```
