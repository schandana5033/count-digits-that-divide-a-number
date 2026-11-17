# count-digits-that-divide-a-number
class Solution {
    public int countDigits(int num) {
        int original = num, count = 0;
        while (num > 0) {
            int digit = num % 10;
            if (digit != 0 && original % digit == 0) count++;
            num /= 10;
        }
        return count;
    }
}
// Time: O(log10 n) | Space: O(1)
