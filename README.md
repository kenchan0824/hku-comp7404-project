The Background
===
This project starts by discussing the traditional methods used in recommendation system.  Then, we will introduce the story of the Netflix Prize competition in 2009.  The collaborative filtering was the winning solution and it was adopted since then. We will conclude this paragraph by comparing those traditional methods introduced with the collaborative filtering and emphasizing the reason why this solution had become the core technology to support tech giants like Amazon, Google, Alibaba, etc.

Problem Formulation
===
In the Netflix problem, we have two entities, the customers and the movies. Customers have rated the movies that they had watched. Netflix, to provide better services and make more profit, would like to know the customers’ preference on other movies that they had not watched. What this technique is expected to do is to infer the missing customers’ preference from other customers to movies preference that had been rated. It will be illustrated with some imagery examples in tables.

The Technical Solution
===
Here we come up with some mathematics. 
|Notation||
|--|--|
|`m`|the number of customers|
|`n`|the number of movies|
|`k`|the number of hidden features that we assigned to movies|
|`Y`|(`m`x`n`) matrix that stores the customers preference to movies with some miss elements|
|`Theta`|(`m`x`k`) matrix representing customers preference to hidden features|
|`X`|(`n`x`k`) matrix representing movies tendency to hidden features|

`Theta` and `X` are parameters that we have to learn in the algorithm.  Actually, the technical interpretation of this problem is finding some `Theta` and `X`, so as to minimize the cost function, which is the mean square error between `Theta` dot `X` transpose and `Y` on all non-missing elements.

The Demonstration
===
We will demonstrate our codes to learn the `Theta` and `X`. With the help of external optimizer, that will be just a few lines. For the audience better understanding on our neat codes, we have to first introduce the concepts of vectorization programming. We will introduce three operations accomplished in vectorization, they are matrix dot product, element-wise operations, and aggregation.

Result Analysis
===
We will investigate the hidden features that will be learnt through collaborative filtering. We will not inform the system with human intelligence about how to classify the movies, or how a customer likes a movie would also like another one. We are interested to know if the machine can obtain this kind of intelligence spontaneously. 

Generalization
===
We think that the use of collaborative filtering should not be restricted to recommend products or services to customers. On the contrary, we will try to formulate the problem in a generative way. We will provide ideas like horse racing and love matching problems to demonstrate on the extensive usage of collaborative filtering.

Summary
===
These should be the takeaway assets of our audience:

 1. Understand the concepts of collaborative filtering
 2. Ability to write a program in vectorization style
 3. Ability to formulate a problem as collaborative filtering problem
 4. Ability to apply collaborative filtering to problems of their own domain
