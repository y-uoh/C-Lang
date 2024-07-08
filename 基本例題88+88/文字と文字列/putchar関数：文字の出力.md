# putchar関数：文字の出力
- 標準出力に文字を一文字分出力する関数
- `getchar`関数から一文字読みだして出力していくときに相性がよい。  
- 引数に文字が代入されている変数を指定するか、特定の文字を出力するときはその文字を指定する

### Sample
```c
#include<stdio.h>
#include<ctype.h>

void main(void) {
	int moji;
	
	while ((moji = getchar()) != EOF) {
		if (isdigit(moji)) {
			putchar('X');	//指定した一文字を出力
		}
		else {
			putchar(moji);	//getchar関数で取得した一文字を出力
		}
		
	}
}
```
