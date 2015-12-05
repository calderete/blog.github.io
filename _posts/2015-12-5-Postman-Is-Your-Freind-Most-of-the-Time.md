---
layout: post
---

###Postman Rocks!
So in the past 3 or 4 weeks we have been building apps with teams of front end engineers, and my workflow goes like this. Come hell or high water GET registration and login working and deploy to heroku. Our front end guys can get plenty of things working <i>in theory</i> but very little meaningfull progress can be made until that is working. Once the app is deployed we are not so dependant on eachother to start some meaningfull hacking. On the back end to test our controllers and associations postman makes that process very easy for us. 

####The Postkraken
Sending data to our local server or our app is a pretty straight forward process postman has a very easy to use gui to get most tasks done. But... what happens when you need to test a method like this

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
{word: => [dog, cat, bird, chicken, honeybadger], category: => animals}

The method works just fine, but I held off deploying the change because I could not figure out how to test it locally. After much googling one of my classmates <a href="http://www.getlosthere.com">Teri</a> had run into a similar problem and showed me how to properly format the postman request, which looks like this

<img src="/images/postman-scap.png =250x" />





