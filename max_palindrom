//#include "stdafx.h"
//#include <fstream>
#include <iostream>
#include <string>
#include <algorithm>
#include <vector>
#include <cmath>
#include <ctime>
#include <map>
#include <set>
#include<random>

#define ll long long

using namespace std;

//ifstream cin("input.txt");
//ofstream cout("output.txt");

int n, mx = 0;
string s;
vector<vector<int> > t;

int main()
{
	cin >> n >> s;
	t.resize(2, vector<int>(n));
	for (int k = 0; k < 2; k++) {
		int l = 0, r = -1;
		for (int i = 0; i < n; i++) {
			int x = (i > r ? 0 : min(t[k][l + r - i + k], r - i + k)) + 1;
			while (i + x - k < n && i - x >= 0 && s[i + x - k] == s[i - x]) {
				x++;
			}
			x--;
			t[k][i] = x;
			mx = max(mx, x * 2 + 1 - k);
			if (i + x - k > r) {
				l = i - x;
				r = i + x - k;
			}
		}
	}
	cout << mx;
	return 0;
}

