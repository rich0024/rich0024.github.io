---
layout: post
title:      "Tournament Winner Javascript"
date:       2021-05-07 19:18:32 +0000
permalink:  tournament_winner_javascript
---


On AlgoExpert, there is a question, 'Tournament Winner'. Usually, after completing a question, I like to check my sollution against the main sollution. Typically, my sollution is somewhat similar in logic, maybe not as optimal but close. However, my answer was completely different but not exactly less optimal. 

Here is my answer:
```
function tournamentWinner(competitions, results) {
  // Write your code here.
	let compInd = 0;
	let resInd = 0;
	var ans = {};
	
	while (compInd < competitions.length) {
		var v = competitions[compInd].reverse()[results[resInd]];
		
		if (v in ans == true) {
			ans[v]++;
		}
		else { ans[v] = 0};
		compInd++;
		resInd++;
	};
	var arr = Object.values(ans).sort((a,b) => b - a);
	return Object.keys(ans).find(key => ans[key] == arr[0]);
}
```

The main answer used a seperate function to tally the winners' score. However I did not find that neccessary.  My idea was to simply go through the tournament and give the winning team a point at the same time. I am not sure which is more optimal, but I am starting to realize that there is not always one correct answer and to not be discouraged if my sollution does not completely match what one is seen as THE correct answer. However, it is important to know why you chose your way and can back it with reason.
