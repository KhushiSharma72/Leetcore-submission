# Two Sum

- Topic: Array
- Pattern: hash-map
- Submitted from: Leetcore
- Submitted at: 2026-07-13T16:52:42.023Z

## Solution

#include <iostream>
#include <vector>
#include <string>
#include <algorithm>

using namespace std;

// Write your C++ code here. Read inputs via cin and print output via cout.
int main() {
    int n;
    cin>>n;
    int arr[100];
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    int target;
    cin>>target;
    vector<int> ans;
    int sum=0;
      for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            if (arr[i] + arr[j] == target) {
                cout << i << " " << j;
                return 0;
            }
        }
    }

    cout << -1;
    return 0;
}
