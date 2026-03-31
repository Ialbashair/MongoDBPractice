# **MongoDBPractice**
## **Query 1: Movies from 1983 with a runtime of more than 200 minutes**
Query:
```ruby
db.movies.find(
  {
    year: 1983,
    runtime: { $gt: 200 }
  },
  {
    _id: 0,
    runtime: 1,
    title: 1,
    year: 1
  }
).sort({ runtime: 1 })
```
Result:

![image1](/image%20copy.png)

## **Query 2: Movies after 2014 with an IMDb rating greater than 9**
Query:
```ruby
db.movies.find({
  year: { $gt: 2014 },
  "imdb.rating": { $gt: 9 }
})
```
Result:

![image2](/image2.png)
