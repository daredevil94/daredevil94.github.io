---
title: "Analyzing Marvel's Network"
date: 2021-12-07T17:21:31+01:00
draft: true
---

Link to explainer notebook:

https://nbviewer.org/github/daredevil94/SGI-Explainer-Notebook/blob/main/notebook.ipynb

Link to datasets:

Characters dataset

https://github.com/daredevil94/SGI-Explainer-Notebook/blob/main/characters.zip

Movies dataset 

https://github.com/daredevil94/SGI-Explainer-Notebook/blob/main/movie_plots.zip

Ever wondered which Marvel character is happiest? Or saddest? Well wait no longer. we found out!

We downloaded the wiki pages of every character and every movie that has been released from the marvel fandom wikipedia. Every hyperlink from one character page to another is deemed as a connection between those two. The text describing the character on the fandom page determines their happiness and sadness. Similarly the movie plots from a movie's fandom page determines the happiness of that movie. 

So let's begin: 

How many connections do characters have, you ask? A plot, showing exactly his, is shown below. 

On average, a character has about 12 connections. 




![image description]({{< baseurl >}}/Picture_3.png)

Well that's all fun and games, but how does it look through the eyes of a social graphs analyst? Well, let's have a look. 

![image description]({{< baseurl >}}/Picture_1.png)


Ugh ugh. Yeah it's not easy being a social graphs analyst. However, we can observe that the network is pretty well-connected. However, are some parts better connected than others, i hear you ask? 

So this Marvel network? Are there any communities? That can be hard to tell from the network graph. Could it maybe be split up to communities that resemble every movie/movie series? Maybe every “main” character will be the core of his/hers own community? 

To reveal the secrets of the connections in the network, we use the Louvain algorithm in order to detect communities within the network.

 It detects 12 communities. 

So let us see. Will every main character have their own community? There are characters that have a movie or a movie series named after them. These are: 

Ant-Man, Black_Panther, Black_Widow, Captain_America, Captain_Marvel, Doctor_Strange, Iron_Man, Spider-Man, Hulk and Thor. 

That is 10 main characters. Besides this we have Eternals and Guardians Of The Galaxy that might make up the 11’th and 12’th community. 
Lets see the communities of the main characters to test out this theory: 


![image description]({{< baseurl >}}/Picture_1_1_same.png)

Turns out, this theory does not hold. Black Panther, Black Widow and Captain America share a community, which negates the theory. However 7/10 main characters have their own community.

How about the following theory then: Characters that appear in the same movies belong to the same community. Similar to the previous theory, but now we do not analyze main characters. 
Lets see a graph of communities and the movies they appear in:


![image description]({{< baseurl >}}/Picture_2.png)

The y axis are marvel movies and the x axis is characters appearing in that movie. Let us examine the graph by looking at community 3, the red one. The red bars are primarily in Spider-Man: Homecoming and Spider-Man: Far From Home, but also we see 1 character appearing in Guardians Of The Galaxy Vol. 2 and 2 characters appearing in The Incredible Hulk. As characters can appear in several movies, the character appearing in Guardians Of The Galaxy Vol. 2 can also appear in a Spider-Man movie. With this in mind we see that the communities look very divided which is exactly what we expected. Actually most of the community appear in the same movie or movie series which was the theory!

![image description]({{< baseurl >}}/Picture_4.png)

We downloaded all the movie pages and cleaned their content in order to keep only the movie plot. From there, we calculated a happiness score per movie. These scores vary from 3.4 to 4.6. 

We find out that the happiest movies per score are: 

*	Ant-Man and the Wasp (4.60)
*	Captain America: The First Avenger (4.33) 
*	The Incredible Hulk (4.30)

The saddest movies are:
*	The Avengers (3.30)
*	Captain Marvel (3.36)
*	Guardians of the Galaxy (3.44)

We can't really conclude something about the sentiment analysis of movies. This is not surprising considering that all marvel movies are quite similar in their plots. Each movie has their part of fighting, heroes and villains, and some jokes. So the sentiment analysis on these movies doesn’t reveal something really relevant.


We decided to focus on the character sentiment analysis, to see if we would have more interesting results. We calculated the sentiment score of the marvel characters by calculating the average happiness score of the words in their biography. We decided to keep only the characters with a certain amount of number in their biography, so the analysis is more relevant and we don’t focus on the small characters.

Here we can have a look at the 10 happiest and saddest characters, according to this analysis:

![image description]({{< baseurl >}}/Picture_7.png)

Among the happiest characters, we find 9 “good guys”, and one who can’t be considered as good or bad (Thaddeus Ross). The happiest character of all Marvel is Michelle Jones, a teenager, girlfriend of Spider-Man.

For the saddest characters, we encounter 5 “bad guys”, 4 “good guys” and one  who can’t be considered as good or bad (Yelena Belova). The principal characteristic that they have in common is that they are all great fighter.

We then thought that a character's happiness and their ability to fight should be calculated separately. For this, we calculated 2 scores for each character. A happiness score, which counts only positive words, and a War score, which counts only negative words, most of which seem related to death and fighting.

![image description]({{< baseurl >}}/Picture_5.png)

We can see now that the war score is more expanded than the happiness score. It makes sense as some characters are great fighters, and other are just scientists, or civilians.

Now that we are more precise about the sentiments of characters, we can look at the sentiment of communities. We took the most important characters of each communities, and then calculated the average happiness score and war score.



![image description]({{< baseurl >}}/Picture_6.png)

WIth:

*	Community 0: SHIELD and Avengers
*	Community 1: Ant-Man
*	Community 2: Guardians of the Galaxy
*	Community 3: Spider-Man
*	Community 4: Shang Xi
*	Community 5: Thor
*	Community 6: Doctor Strange
*	Community 7: Iron Man
*	Community 8: Captain America
*	Community : Black Panther
*	Community 10: Captain Marvel

