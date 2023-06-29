# Leetcode-Training-Repository
This is for recording the code training.
给你两个字符串 word1 和 word2 。请你从 word1 开始，通过交替添加字母来合并字符串。如果一个字符串比另一个字符串长，就将多出来的字母追加到合并后字符串的末尾。

返回 合并后的字符串 。
class Solution {
public:
    string mergeAlternately(string word1, string word2) {
        int word1_length = word1.length();
        int word2_length = word2.length();
        string output_string = "";

        int i=0;
        int j=0;
        while(i<word1_length || j<word2_length){//循环条件
            if(i<word1_length){//保证在指定的位置放入数组指定的元素
                output_string+=word1[i];
            }
            i++;
            if(j<word2_length){
                output_string+=word2[j];
            }
            j++;
        }
        return output_string;
    }
};
