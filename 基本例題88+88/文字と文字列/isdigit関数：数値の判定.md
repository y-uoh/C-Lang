# isdigit関数：数値の判定
- 文字が数値であるか判定する関数
- ヘッダ：`ctype.h`
- 引数：判定したい文字
- 戻り値：数値の場合、0以外、それ以外0

### Sample
```c
#include<stdio.h>
#include<ctype.h>

void main(void) {
	int moji;
	
	while ((moji = getchar()) != EOF) {
		if (isdigit(moji)) {  //変数mojiが数値だったら0以外を返すため真となり、それ以外は0を返すため偽となる
			putchar('X');
		}
		else {
			putchar(moji);
		}
		
	}
}
```