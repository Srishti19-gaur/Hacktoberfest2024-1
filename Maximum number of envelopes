// C++ program for the above approach
#include <bits/stdc++.h>
using namespace std;

// Function that returns the maximum
// number of envelopes that can be
// inserted into another envelopes
int maxEnvelopes(vector<vector<int> > envelopes)
{
	// Number of envelopes
	int N = envelopes.size();

	if (N == 0)
		return N;

	// Sort the envelopes in
	// non-decreasing order
	sort(envelopes.begin(),
		envelopes.end());

	// Initialize dp[] array
	int dp[N];

	// To store the result
	int max_envelope = 1;

	dp[0] = 1;

	// Loop through the array
	for (int i = 1; i < N; ++i) {
		dp[i] = 1;

		// Find envelopes count for
		// each envelope
		for (int j = 0; j < i; ++j) {

			if (envelopes[i][0] > envelopes[j][0]
				&& envelopes[i][1] > envelopes[j][1]
				&& dp[i] < dp[j] + 1)
				dp[i] = dp[j] + 1;
		}

		// Store maximum envelopes count
		max_envelope = max(max_envelope,
						dp[i]);
	}

	// Return the result
	return max_envelope;
}

// Driver Code
int main()
{
	// Given the envelopes
	vector<vector<int> > envelopes
		= { { 4, 3 }, { 5, 3 }, { 5, 6 }, { 1, 2 } };

	// Function Call
	cout << maxEnvelopes(envelopes);

	return 0;
}
