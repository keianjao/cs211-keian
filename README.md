# cs211-keian

int countWays(int n) {

    // to store values of last two states 
    int prev1 = 1;
    int prev2 = 1;

    for (int i = 2; i <= n; i++) {
        int curr = prev1 + prev2;
        prev2 = prev1;
        prev1 = curr;
    }

    // In last iteration final value
    // of curr is stored in prev.
    return prev1;
}
//Driver Code Starts

int main() {
    int n = 4;
    printf("%d
", countWays(n));
    return 0;
}
