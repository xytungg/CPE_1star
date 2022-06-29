# (UVA10929) You can say 11 2022/06/29
>Tips：數學公式解、迴圈、字串
Q：判斷奇數位和-偶數位是否為11的倍數
Eg：5038297，7+2+3+5=17，9+8+0=17，兩數相減為0，是11的倍數
```python
while True:
	i=int(input())
	if i==0:break
	if i%11==0:print(str(i)+" is a multiple of 11.")
	else:print(str(i)+" is not a multiple of 11.")
```
