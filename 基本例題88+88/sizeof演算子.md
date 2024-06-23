# sizeof演算子
- 型のメモリ領域の大きさ、変数のメモリ領域の大きさを得ることができる演算子
- 使い方は`sizeof<型名>`、あるいは`sizeof<変数名>`とする
- printfなどの出力系関数で表示するには、`%zu`というフォーマット指定子を使う。ただ、整数値を扱うので`%d`でも出力できる。 
- char型の大きさは1バイト固定だが、他の型の大きさは処理系によって異なる。long型は本だと8バイトになっているが、自分の環境は4バイト
    
### Sample
```c
#include<stdio.h>

void main() {
	int i;
    
	printf("int : %zu byte\n", sizeof(int));    //int型のメモリサイズを表示
	printf("int i :%zu byte\n", sizeof(i));     //変数iのメモリサイズを表示
	printf("char : %zu byte\n", sizeof(char));
	printf("short : %zu byte\n", sizeof(short));
	printf("long : %zu byte\n", sizeof(long int));
	printf("float : %zu byte\n", sizeof(float));
	printf("double : %zu byte\n", sizeof(double));
```

 