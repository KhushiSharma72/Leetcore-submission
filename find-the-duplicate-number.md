# Find the Duplicate Number

- Topic: Array
- Pattern: fast-slow-pointers
- Submitted from: Leetcore
- Submitted at: 2026-07-13T17:06:48.911Z

## Solution

#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
#include<unordered_map>

using namespace std;

// Write your C++ code here. Read inputs via cin and print output via cout.
int main() {
    int n;
    cin>>n;
    int arr[100];
    for(int i=0;i<n;i++){
      cin>>arr[i];
    }
    unordered_map<int,int>mpp;
    for(int i = 0; i < n; i++){
        mpp[arr[i]]++;

        if(mpp[arr[i]] == 2){
            cout << arr[i];
            return 0;
        }
    }
}
