# NORMALIZATION

#include<iostream>
#include<string.h>
using namespace std;

int main(){
	string a;
	cin >> a;
	for (int i=0; i < a.size() ; i++){
		if ((a[i]>= 'a' && a[i] <= 'z')||(a[i]>= 'A' && a[i] <= 'Z')){
			continue;
		}
		else a[i] =  ' ';
	}
	for (int i=0; i < a.size() ; i++){
		if (a[i]>= 'A' && a[i] <= 'Z'){
			a[i] +=32;
		}
	}
	for (int i=a.size()-2; i >=0 ; i--){
		if (a[i]== ' ' && a[i+1] == ' '){
			a[i+1]= '';
		}
		if (a[i]== ' '&& a[i+1] >= 'a' && a[i+1] <= 'z') {
			a[i+1]-=32; 
		}
	}
	cout << a;
	return 0;
}
