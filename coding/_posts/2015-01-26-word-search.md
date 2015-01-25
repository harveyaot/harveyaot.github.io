---
layout: post
title: word search solution
comments: true
---
The wired thing is that I used visit bool array to record elments visit infomation and It suggests me TLE error.However after I use board[i][j] ^= 0x80 instead [reference](https://oj.leetcode.com/discuss/22848/why-my-solution-with-dfs-is-tle) accepted. the new solution doesn't change the time complexity. This solution costs around 60ms and I saw many cpp solution cost only  10ms. Where can I continue to improve my solution ?

``` c++

class Solution {

public:

   
    bool search(vector<vector<char> > &board, string word,int i,int j,int n){
        int length = word.size();
        int height = board.size();
        int width = board[0].size();
        
        if (i == height || j == width || i < 0 || j < 0){
            return false;
        }    
        
        if ( n == length - 1)
            if (board[i][j] == word[n]) return true;
            else return false;
        
        if (board[i][j] != word[n]){
            return false;           
        }else{
            board[i][j] ^= 0x80;
            // forward left
            if (search(board,word,i,j-1,n+1)) return true;
            // forward right 
            if (search(board,word,i,j+1,n+1)) return true;
            // forward up 
            if (search(board,word,i-1,j,n+1)) return true;
            // forward down 
            if (search(board,word,i+1,j,n+1)) return true;
        }
        board[i][j] ^= 0x80;
        return false;
        
    }
    
    bool exist(vector<vector<char> > &board, string word) {
          //
        int length = word.size();
        if (length==0) return true;
        
        int height = board.size();
        int width = board[0].size();
        
        if (height ==1 && width ==1 ) return (length == 1 && board[0][0] == word[0]);

        for(int i=0; i < height; i++)
            for(int j=0; j < width; j++){
            
                if (search(board,word,i,j,0)){
                    return true;
                }
            }
            return false;
    }
};
```
