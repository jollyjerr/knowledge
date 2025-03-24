# Recommender System

- Popularity: recommend most popular to everyone
- Content based: use hand engineered attributes to associate similar content

Music genome project from Pandora: https://www.pandora.com/about/mgp

- Collaborative filtering: recommend items chosen by similar users

Can suffer from _cold start_ problem, need some info about the user to recommend
anything. Scales with latent factor modeling and supervised models.

## Similarity Measures

Data given in utility matrix - normally sparse. You can impute with the average
rating for each user.

Get data: buy or not buy, explicit ratings.

User-user similarity: users are similar if they buy the same items.

Item-item similarity: items are similar if they are bought by similar users.

- Cosine similarity

```
a and b are vectors with buy or rating info for each item

cos_sim(a, b) = a @ b / ||a|| ||b||

||a|| = sqrt(sum a[i]^2) # the magnitude

result: -1 to 1
```

- Jaccard similarity

Good for binary data like buy or not buy.

```
jaccard(a, b) = S[a] intersect S[b] / S[a] union S[b]
```

- Distance based: Manhattan, Euclidean, Minkowski
- Pearson Correlation

## Scale

Data is often very large and very sparse, so time complexity of these operations
can become a huge problem at scale.

It can be helpful to reduce the dimensions of data first or cluster multiple
items into one "item" that represents a cluster.
