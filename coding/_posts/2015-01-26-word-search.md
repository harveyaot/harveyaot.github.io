---
layout: post
title: word search solution
comments: true
---
The wired thing is that I used visit bool array to record elments visit infomation and It suggests me TLE error.However after I use board[i][j] ^= 0x80 instead [reference](https://oj.leetcode.com/discuss/22848/why-my-solution-with-dfs-is-tle) accepted. the new solution doesn't change the time complexity. This solution costs around 60ms and I saw many cpp solution cost only  10ms. Where can I continue to improve my solution ?

{% gist ac24d130fbe835fd43ea %}

