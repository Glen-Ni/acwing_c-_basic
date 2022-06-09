写起来太浪费时间里，挑几题写写

- 720. 连续整数相加

  可以用逗号运算符，可以用公式
  ```c++
    while(cin>>n,n<=0){}
    cout<<(a+a+n-1)*n/2;
  ```

  ```c++
  #include <cstdio>

  using namespace std;

  int main()
  {
      int a,n;
      scanf("%d%d", &a, &n);
      while(n <= 0)
      {
          scanf("%d", &n);
      }
      int result = 0;
      for(int i = a; i < a + n; i ++) {
          result += i;
      }
      printf("%d", result);
      
      return 0;
  }
  ```

- 724. 约数
  ```C++
  #include <iostream>

  using namespace std;

  int main()
  {
      int n;
      cin >> n;
      for(int i = 1; i <= n; i++) {
          if(n%i == 0) {
              cout << i << endl;
          }
      }
      return 0;
  }
  ```

725. 完全数
  - 这题还是有点意思的, 直接算容易TLE
  - 如果a是x的约数，x/a必然也是x的约数，所以只要算小于等于sqrt(x)的即可
  - 注意第一个数是数据个数,没用
  - 注意是不与自己相同的约数，所以1不是完全数
  ```c++
  #include <iostream>

  using namespace std;

  int main()
  {
      int s,n,x;
      cin >> n;
      while (cin >> x) {
          s = 0;
          for(int i = 1; i * i <= x; i++)
          {
              if(x%i == 0)
              {
                  s += i;
                  if(i * i != x && i != 1) s += x / i;
              }
          }
          if (s == x && x != 1) cout << x << " is perfect" << endl;
          else cout << x << " is not perfect" << endl;
      }
      
      return 0;
  }
  ```