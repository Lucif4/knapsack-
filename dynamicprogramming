
  #include <iostream>
  using namespace std;
  int main()
  {
      int n,W;
      cin>>n>>W;
      int val[n+1],wt[n+1];
      for (int i = 1; i <= n; i++)
      {
          cin>>val[i]>>wt[i];
      }
      int V[n+1][W+1];
      // tao co so quy hoach dong
      for (int w = 0; w<=W ; w++) V[0][w] = 0;
      for (int i = 0; i<=n; i++) V[i][0] = 0;

      // Tao bang phuong an su dung cong thuc truy hoi
      for (int i = 1;i<=n;i++)
      {
          for (int w=1;w<=W;w++)
          {
              if (wt[i]>w) V[i][w] = V[i-1][w];
              else {V[i][w] = max(V[i-1][w],val[i] + V[i-1][w-wt[i]]);}
          }
      }
      cout<<V[n][W]<<endl;
      int k = n, l = W;
      // truy vet
      while (k!=0 && l!=0)
      {
          if (V[k][l] != V[k-1][l])
          {
              cout <<k<<" ";

              l =l- wt[k];
              k = k -1;
          } else
          {
              k = k - 1;
          }
      }
      return 0;
  }
  // Lucif4 17/8/2021
