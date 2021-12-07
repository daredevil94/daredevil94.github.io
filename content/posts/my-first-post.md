---
title: "My First Post"
date: 2021-12-07T17:21:31+01:00
draft: true
---

![image description]({{< baseurl >}}/Picture_1.png)

So this marvel community? How is it connected? That can be hard to tell from the network graph. Can it be split up to communities that resemble every movie/movie series? Maybe every “main” character will be the core of his/hers own community? 

To reveal the secrets of the connections in the network, we use the Louvain algorithm to detect communities within the network. It detects 12 communities. 
So let us see. Will every main character have their own community. There are characters that have a movie or a movie series named after them. These are: Ant-Man, Black_Panther, Black_Widow, Captain_America, Captain_Marvel, Doctor_Strange, Iron_Man, Spider-Man, Hulk and Thor. That is 10 main characters. Besides this we have Eternals and Guardians Of The Galaxy that might make up the 11’th and 12’th community. 
Lets see the communities of the main characters to test out this theory: 

![image description]({{< baseurl >}}/Picture_1_1_same.png)


Turns out, this theory does not hold. Black Panther, Black Widow and Captain America share a community, which negates the theory. However 7/10 main characters have their own community.

How about this theory then. Characters that appear in the same movies are in the same community. Similar to the previous theory, but now we do not analyze main characters. 
Lets see a graph of communities and the movies they appear in:

![image description]({{< baseurl >}}/Picture_2.png)

The y axis are marvel movies and the x axis is characters appearing in that movie. Lets examine the graph by looking at community 3, the red one. The red bars are 
And it looks very divided which is exactly what we expect 


![image description]({{< baseurl >}}/Picture_3.png)


![image description]({{< baseurl >}}/Picture_4.png)


plot. From there, we calculated a happiness score per movie. These scores vary from 3.4 to 4.6. 

We find out that the happiest movies per score are:

*	Ant-Man and the Wasp (4.60)
*	Captain America: The First Avenger (4.33) 
*	The Incredible Hulk (4.30)

The saddest movies are:

*	The Avengers (3.30)
*	Captain Marvel (3.36)
*	Guardians of the Galaxy (3.44)

We can't really conclude something about the sentiment analysis of movies. This is not surprising considering that all marvel movies are quite similar in their plots. Each movie has their part of fighting, heroes and villains, and some jokes. So the sentiment analysis on these movies doesn’t reveal something really relevant.


We decided to focus on the character sentim

![image description]({{< baseurl >}}/Picture_5.png)


![image description]({{< baseurl >}}/Picture_6.png)


