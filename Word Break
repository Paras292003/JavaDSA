import java.util.List;

public class WordBreak {
    public boolean wordBreak(String s, List<String> wordDict) {
        boolean[] dp = new boolean[s.length() + 1];
        dp[0] = true;
        
        for (int i = 1; i <= s.length(); i++) {
            for (String word : wordDict) {
                if (i >= word.length() && dp[i - word.length()]) {
                    if (s.substring(i - word.length(), i).equals(word)) {
                        dp[i] = true;
                        break;
                    }
                }
            }
        }
        
        return dp[s.length()];
    }
    
    public static void main(String[] args) {
        WordBreak solution = new WordBreak();
        String s = "leetcode";
        List<String> wordDict = List.of("leet", "code");
        boolean canBreak = solution.wordBreak(s, wordDict);
        System.out.println("Can be segmented: " + canBreak);
    }
}
