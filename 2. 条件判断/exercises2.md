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

- 668. 游戏时间 2

  我这个方法有点巧妙的哦，不愧是我

  ```c++
  #include <cstdio>

  using namespace std;

  int main() {
      int h1,s1,h2,s2,t1,t2;
      scanf("%d%d%d%d", &h1,&s1,&h2,&s2);
      t1 = h1 * 60 + s1;
      t2 = h2 * 60 + s2;
      if (t1 >= t2){
          t2 += 60 * 24;
      }
      printf("O JOGO DUROU %d HORA(S) E %d MINUTO(S)", (t2 - t1) / 60, (t2 - t1) % 60);

      return 0;
  }
  ```

- 672. 税

  ```C++
  #include<cstdio>

  using namespace std;

  int main(){
  		double a;
  		scanf("%lf", &a);
  		if(a>0&&a<=2000.0) printf("Isento");
  		else if(a>2000.0&&a<=3000) printf("R$ %.2lf",(a-2000)*0.08);
  		else if(a>3000.0&&a<=4500) printf("R$ %.2lf",(a-3000)*0.18+80);
  		else if(a>4500.0) printf("R$ %.2lf",(a-4500)*0.28+350);
  		return 0;
  }
  ```

- 663. 简单排序
	```c++
	#include<cstdio>
	#include<iostream>
	using namespace std;
	int main()
	{
			int a,b,c;
			cin>>a>>b>>c;
			int x,y,z;
			x=max(a,max(b,c));
			y=min(a,min(b,c));
			z=a+b+c-x-y;
			cout<<y<<endl;
			cout<<z<<endl;
			cout<<x<<endl;
			cout<<endl;
			cout<<a<<endl;
			cout<<b<<endl;
			cout<<c<<endl;
			return 0;
	}
	```

- 658. 一元二次方程公式

	无聊
	```c++
	#include <cstdio>
	#include <math.h>

	using namespace std;

	int main()
	{
			double a,b,c,d;
			scanf("%lf%lf%lf", &a, &b, &c);
			d = b * b - 4 * a * c;
			if(d < 0 || a==0){
					printf("Impossivel calcular");
					return 0;
			}
			printf("R1 = %.5lf\n", (-b+sqrt(d))/2/a);
			printf("R2 = %.5lf\n", (-b-sqrt(d))/2/a);
			
			return 0;
	}
	```

- 661. 平均数3

	不值得花时间写
	```c++
	#include<bits/stdc++.h>
	using namespace std;

	int main()
	{
			double a,b,c,d,n,m,x;
			cin>>a>>b>>c>>d;
			m=(a*2.0+b*3.0+c*4.0+d)/10.0;
			cout<<fixed<<setprecision(1)<<"Media: "<<m<<endl;
			if(m>=7.0)cout<<"Aluno aprovado."<<endl;
			if(m<5.0)cout<<"Aluno reprovado."<<endl;
			if(m>=5.0&&m<7.0){
					cout<<"Aluno em exame."<<endl;
					cin>>n;
					cout<<"Nota do exame: "<<n<<endl;
					x=(m+n)/2;
					if(x>=5.0)cout<<"Aluno aprovado."<<endl;
					if(x<5.0)cout<<"Aluno reprovado."<<endl;
					cout<<fixed<<setprecision(1)<<"Media final: "<<x<<endl;
			}
	}
	```