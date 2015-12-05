---
layout: post
---

###Postman Rocks!
So in the past 3 or 4 weeks we have been building apps with teams of front end engineers, and my workflow goes like this. Come hell or high water GET registration and login working and deploy to heroku. Our front end guys can get plenty of things working <i>in theory</i> but very little meaningfull progress can be made until that is working. Once the app is deployed we are not so dependant on eachother to start some meaningfull hacking. On the back end to test our controllers and associations postman makes that process very easy for us. 

###The Postkraken
Sending data to our local server or our app is a pretty straight forward process. Postman has a very easy to use gui to get most tasks done. But... what happens when you need to test a method like this

{% highlight ruby %}
def creates
	@words = params[:words]
	@words.map do |word|
		current_user.words.create!(word: word, category: params[:category])
   end
  @words= current_user.words
	render "word_create.json.jbuilder"
end
{% endhighlight ruby %}

This method is dealing with a bit of json that looks like this
```{
		word: => [dog, cat, bird, chicken, honeybadger], 
		category: => animals
	 }```

The method works just fine, but I held off deploying the change because I could not figure out how to test it locally. Copying and pasting the horrendous errors postman was throwing out when I tried to pass a variable of an array with the key ```word:``` actually broke google. Fortunatly one of my classmates <a href="http://www.getlosthere.com">Teri</a> had run into a similar problem and showed me how to properly format the postman request, which looks like this.

<img src="/images/postman-scap.png" style="width: 600px;"/>


###Victory!!!

So yeah I got to strut around for like ten minutes...feeling like a computer ninja! Front end can add as many words into a category as they want with a single reqeust and my code will take care of the rest.

###The Next Postkraken

Ok so my team can create words with a single request...great. Now they want to edit in a single request. In <i>theory</i> for me not so difficult to figure out...maybe. Long story short here is the javascript object (json) they would send me and the way to simulate such a reqeust in postman.

```{
		words: => [
							{id: => 1, new: => "kola"}, 
							{id: => 2, new: => "kangaroo"},
							{id: => 3, new: => "tiger"},
							{id: => 4, new: => "dragon"},
							{id: => 5, new: => "python"},
							 ]```

Which will hit this method in my controller

{% highlight ruby %}

def edit
	params[words:].each do |new_word|
		word = Word.find(new_word[:id])
		word.update(word: new_word[:new])
	end
end

{% endhighlight ruby %}

And here is the way to properly format this

<img src="/images/postman-2-scap.png" style="width: 600px;"/>



















}





