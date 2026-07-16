# Plus One

- Topic: Array
- Pattern: simulation
- Submitted from: Leetcore
- Submitted at: 2026-07-16T17:34:24.043Z

## Solution

#include <iostream>
#include <vector>
#include <string>
#include <algorithm>

using namespace std;

// Write your C++ code here. Read inputs via cin and print output via cout.
#include <iostream>
#include <vector>
using namespace std;

class Solution {
public:
    vector<int> plusOne(vector<int>& digits) {
        for (int i = digits.size() - 1; i >= 0; i--) {
            if (digits[i] < 9) {
                digits[i]++;
                return digits;
            }
            digits[i] = 0;
        }

        digits.insert(digits.begin(), 1);
        return digits;
    }
};

int main() {
    int n;
    cin >> n;

    vector<int> digits(n);

    for (int i = 0; i < n; i++) {
        cin >> digits[i];
    }

    Solution obj;
    vector<int> result = obj.plusOne(digits);

    for (int x : result) {
        cout << x << " ";
    }

    return 0;
}
