#include <bits/stdc++.h>
using namespace std;
#define ll long long

int gcd(int a,int b) {
	if(b == 0) 
		return a;
	return gcd(b, a % b);
}

int lcm(int a,int b) {
	return (a / gcd(a,b) * b);
}

int maximum_element(int arr[],int n) {
	int temp = arr[0];
	for(int i = 1; i < n; ++i) {
		if(arr[i] > temp) temp = arr[i];
	}
	return temp;
}

int minimum_element(int arr[],int n) {
	int temp = arr[0];
	for(int i = 1; i < n; ++i) {
		if(arr[i] < temp) temp = arr[i];
	}
	return temp;
}

int in_binary(int n) {
	int binary = 0,rem = 0,i = 1;
	while(n != 0) {
		rem = n % 2;
		n /= 2;
		binary += rem * i;
		i *= 10;
	}
	return binary;
}


void solve() {
	
}

int main() {
	int T;
	cin >> T;
	while(T--)
		solve();
	return 0;
}
