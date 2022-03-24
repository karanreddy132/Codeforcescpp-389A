# Codeforcescpp-389A
#include <bits/stdc++.h>
using namespace std;

int main() {
	int n,a[101],sum(0);
  cin >> n;
  for(int i=0;i<n;i++)
    cin >> a[i];
  
  sort(a,a+n);
  int i = 1;
  while(i<=n-1){
    while(a[i] > a[i-1]){
      a[i]-=a[i-1];
      
      if(a[i] < a[0])
        i = 1;
      sort(a,a+n);
    }
    i++;
  }
  cout << accumulate(a,a+n,sum);
	return 0;
}
