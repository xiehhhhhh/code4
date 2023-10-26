# code4
#include<iostream> 
using namespace std;
const int v[6] = {1,5,10,50,100,500};//硬币面值
int c[6];//硬币数量
int A;
 
void Solve() {
	int ans = 0;
	for(int i = 5; i >= 0; i--)
	 {
		int t = min(A / v[i],c[i]);
		A -= t * v[i];
		ans += t;
	}
	cout<<ans;
}
 
int main(void)
 {
	for(int i = 0; i < 6; i++)
	 {
		cin>>c[i];
	}
	cin>>A;
	Solve();
	return 0;
}
