---
layout: post
title:  "Rearrange characters of a string to create all possible combinations"
date:   2013-03-18 00:00:00 -0800
---
> Governments tend not to solve problems, only rearrange them. - Ronald Reagan

How to take a word(string) and rearrange its letters to create all possible combinations? Lets say we want to use the word ‘goal’ and list out all possible words that can be made by rearranging the letters of the word ‘goal’. Take the first letter ‘g‘ and then create permutations and combinations of the balance letters ‘oal‘ and append them to ‘g‘.

| g | oal |
|---|-----|
|   | ola |
|   | alo |
|   | aol |
|   | loa |
|   | lao |

Then take go and create create permutations for the balance letters ’al‘ and append them to ‘go‘.

| go | al |
|----|----|
|    | la |

Then we take goa and l

| goa | l |
|-----|---|
|     |   |

This is done for each of the letters. As you can see, with each letter, the permutations will reduce for the subsequent letters. The parameters that are passed to our recursive function are a prefix that will be used to prepend (starting with an empty string) AND the balance letters of the word.

Here’s the function in JavaScript:

{% highlight javascript %}
function rearrange(word) {
	var words = [];
  
  if (!word || typeof word !== 'string')
  	return 'Invalid input!';

	function helper(prefix, str) {
		if (str.length === 1) {
			if (words.indexOf(prefix + str) < 0) {
				words.push(prefix + str);
			}
		} else {
			str.split('').forEach(function(letter, index) {
				var substr = str.slice(0, index) + str.slice(index + 1);
				helper(prefix + letter, substr);
			});
		}
	}

	helper('', word);
	return words;
}

var words = rearrange('goal');
console.log(words);
{% endhighlight %}