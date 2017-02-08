---
layout: post
title: wordbreak [leetcode]
tags : [leetcode]
language: python
comments: true
---

使用纯搜的办法代码如下：

~~~python
class Solution:
    # @param s, a string
    # @param dict, a set of string
    # @return a boolean
    def wordBreak(self, s, dict):
        
        if not s:
            return True
            
        for i in xrange(len(s)):
            if s[:i+1] in dict:
                res = self.wordBreak(s[i+1:],dict)
                if res: return True 
            
        return False
~~~

提示 TLE错误，思考如何使用DP（Dynamic Programming）的方法来解决问题，自己想没想出来，忍不住偷看了答案，比想象的还要简单，关于DP的题目做的还是太少，导致了，导致思考的时候，头脑可寻找的模板太少。果不其然，DP的题目，从来离不开数组，只是这次数组是个Boolean 数组。

~~~python
def word_break(s, words):
    d = [False] * len(s)    
    for i in range(len(s)):
        for w in words:
            if w == s[i-len(w)+1:i+1] and (d[i-len(w)] or i-len(w) == -1):
                d[i] = True
    return d[-1]
~~~
