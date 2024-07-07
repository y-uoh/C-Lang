# unsigned演算子
- データ型の符号なしで指定してくれる演算子
    
### Sample
```c
#include<stdio.h>

void main(void){

printf("\n\n");
printf("unsigned int : %zu byte\n", sizeof(unsigned int));  //符号なしint型のメモリサイズを出力  
printf("unsigned short : %zu byte\n", sizeof(unsigned short));
printf("unsigned long : %zu byte\n", sizeof(unsigned long));

}
```
