# Contains Duplicate

- Topic: Array
- Pattern: hash-set
- Submitted from: Leetcore
- Submitted at: 2026-07-13T16:58:14.865Z

## Solution

#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
#include <unordered_set>

using namespace std;

// Write your C++ code here. Read inputs via cin and print output via cout.
int main() {
    int n;
    cin >> n;

    vector<int> nums(n);

    for (int i = 0; i < n; i++) {
        cin >> nums[i];
    }

    unordered_set<int> s;

    for (int i = 0; i < n; i++) {
        if (s.find(nums[i]) != s.end()) {
            cout << "true";
            return 0;
        }
        s.insert(nums[i]);
    }

    cout << "false";

    return 0;
}
