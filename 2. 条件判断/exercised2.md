- 671

  ```c++
  #include<iostream>
  using namespace std;
  int main()
  {
      int x;
      cin>>x;
      if(x==61)
          cout<<"Brasilia";
      else if(x==71)
          cout<<"Salvador";
      else if(x==11)
          cout<<"Sao Paulo";
      else if(x==21)
          cout<<"Rio de Janeiro";
      else if(x==32)
          cout<<"Juiz de Fora";
      else if(x==19)
          cout<<"Campinas";
      else if(x==27)
          cout<<"Vitoria";
      else if(x==31)
          cout<<"Belo Horizonte";
      else
          cout<< "DDD nao cadastrado";
      return 0;
  }
  ```

- 662.点的坐标

  ```c++
  #include <iostream>

  using namespace std;

  int main()
  {
      double x,y;
      cin >> x >> y;

      if (x > 0 && y > 0) cout << "Q1" << endl;
      else if (x > 0 && y < 0) cout << "Q4" << endl;
      else if (x < 0 && y > 0) cout << "Q2" << endl;
      else if (x < 0 && y < 0) cout << "Q3" << endl;
      else if (x == 0 && y != 0) cout << "Eixo Y" << endl;
      else if (x != 0 && y == 0) cout << "Eixo X" << endl;
      else  cout << "Origem" << endl;

      return 0;
  }
  ```

- 666. 三角形类型

  还挺麻烦，注意不能组成三角形就直接 return
  可以用 `swap(a, b)`直接交换 a 和 b...

```c++
#include <cstdio>

using namespace std;

int main()
{
    double a,b,c;
    scanf("%lf %lf %lf", &a, &b, &c);
    double max,s1,s2;

    if(a >= b )
    {
        max = a;
        s1 = b;
    }
    else {
        max = b;
        s1 = a;
    }
    if (c >= max)
    {
        s2 = max;
        max = c;
    } else {
        s2 = c;
    }

    if (max >= s1 + s2 )
    {
        printf("NAO FORMA TRIANGULO\n");
        return 0;
    }
    if (max * max == (s1 * s1 + s2 * s2) ) printf("TRIANGULO RETANGULO\n");
    if (max * max > (s1 * s1 + s2 * s2) ) printf("TRIANGULO OBTUSANGULO\n");
    if (max * max < (s1 * s1 + s2 * s2) ) printf("TRIANGULO ACUTANGULO\n");
    if (max == s1 && s1 == s2 ) printf("TRIANGULO EQUILATERO\n");
    else if (max == s1 || s1 == s2 || max == s2) printf("TRIANGULO ISOSCELES");

    return 0;
}
```
