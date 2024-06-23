# Switch文
- 整数の定数と等しいかどうかで場合分けできるときには`switch文`が便利
- `break文`を忘れないようにする。break文がないと次のcaseラベルの処理を続けて実行してしまう。
- `defaultラベル`は`caseラベル`に当てはまらないときにの処理で、概ね誤った入力値などを処理するエラー処理となり、return文でプログラムが終了するケースが多い  

### Sample
２つの実数を入力し、さらに四則演算のどれかを整数で指定するとその計算結果を表示するプログラム
```c
#include<stdio.h>

void main() {
	double x, y;
	int i;

	printf("x? > ");
	scanf("%lf", &x);
	printf("y? > ");
	scanf("%lf", &y);
	printf("演算を選んで下さい：\n");
	printf("1：加算　2：減算　3：乗算　4：除算\n");
	scanf("%d", &i);
	
	switch (i) {  //引数には整数値が代入された変数を指定することが多い。演算文は入れられない
		case 1:
			printf("答え %f", x + y);
			break;  //処理が実行されたらbreakでswich文から抜けるようにする
		case 2:
			printf("答え %f", x - y);
			break;
		case 3:
			printf("答え %f", x * y);
			break;
		case 4:
			printf("答え %f", x / y);
			break;
		default:    //caseラベルにどれも当てはまらないときに実行される処理を記述する。概ねエラーに該当する
			printf("演算指定が間違っています。\n");
			return 0;   //エラーなので代替returnで処理を終わらせることが多い
	}
	return 0;
}
```