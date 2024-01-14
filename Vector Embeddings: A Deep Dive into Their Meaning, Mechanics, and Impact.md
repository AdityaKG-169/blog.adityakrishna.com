In the ever-evolving landscape of machine learning and natural language processing, vector embeddings stand out as a powerful and versatile concept. These mathematical representations of words, phrases, or entities have become the backbone of various applications, offering a nuanced understanding of language and context.

In this blog post, we will unravel the essence of vector embeddings, exploring what they are, how they work, their significance, and the diverse use cases that make them indispensable in the realm of artificial intelligence.

Let's begin!

### Why do we need Vector Embeddings?

Before we deep dive into the technicals of vector embeddings, it's crucial to understand the 'why' behind them.

Vector embeddings are the backbone of most of the search applications, chatbots, AI assistants you use today. They provide a way to mathematically depict the **meaning** behind your query and find the most relevant response for it. Without them, we are just limited to keyword based search (matching keywords in your query with the available data).

Vector embeddings make it possible to generate results that are much more tailored towards your query by understanding the meaning behind your query. Let me demonstrate this with a few examples.

Let's say you run the following query: "Apple's latest products". Without proper context, in your query, Apple could mean both the company as well as the fruit. For the search engine to generate correct and relevant responses, it needs to understand the context and not just do keyword matching.

For second example, let's take 2 sentences.

Sentence 1: "Best restaurants in Paris"

Sentence 2: "Top dining experiences in the heart of the French capital."

As you can see, these 2 sentences mean exactly the same, but don't share any relevant keywords. A simple keyword matching algorithm would have resulted in an utterly wrong result. Vector embeddings on the other hand, capture the meaning behind the data.

### What are Vector Embeddings?

Before we understand what vector embeddings are, let's have a brief look at vectors. Think of vector like an arrow. It has a certain length, and at all times it point towards a direction, could be anywhere. That's it. This is a vector. You can think of the vector as a point in space, with the “direction” being an arrow from the origin to that point in the vector space**.**

Below is the image representing a vector of length √2 that has an angle of 45 degrees with both the x and the y coordinate.

![Image of a vector in x-y plane](https://cdn.hashnode.com/res/hashnode/image/upload/v1705172562597/fb024380-cc48-4df3-8899-2c9737bdbc87.png align="left")

Programatically, we can denote vectors as:

```python
# Example 1
vector_1 = [1,1] # (1,1) in x-y plane

# Example 2
vector_2 = [-2,5,2 .... n] # some point in an n-dimensional space
```

In a space that has multiple vectors, each vector has a certain distance between itself and the others. In the figure below, you can see that in the plane, there are vectors that have different magnitudes and directions. Some are closer to each other while the others are far apart. We'll utilise these properties to do lots of interesting stuff.

![Vectors of different magnitude and direction in x-y plane](https://cdn.hashnode.com/res/hashnode/image/upload/v1705173623452/d245c63b-4303-4c9f-95dc-35b20e671a9d.png align="left")

Now that we've understood what vectors are, let's use this knowledge to learn about vector embeddings.

Let's say we want to build a search engine that retrieves the data based upon an algorithm that does't rely on keyword matching but understands the meaning behind your query. To capture the semantic or the meaning that, we need to convert it into vector. Now, this process isn't straightforward. We need to use an **embedding model** to convert your query (or any data for that matter) into vectors. These embedding models take as input some information (text, image, audio etc.) and convert it into a vector that could be of some variable dimension (each model has it's own properties).

There are several embedding models in the industry that serve their own purpose. You can even convert audio, images into vectors. There are models for that too. Some popular embedding models are: Word2Vec (by Google), Ada (by OpenAI). These embedding models are built by passing a large amount of **labeled data** to a neural network.

Vectors that are close together have a contextual similarity, whereas far-apart vectors are different from one another. That’s what gives our vector **meaning** — its relationship with other vectors in the vector space depends on how the embedding model “understands” the domain it was trained on.

### How to use Vector Embeddings?

Coming back to our search engine example; we want to retrieve information that suits the context of users' query. We have already discussed how we'll be using vectors for this. But how exactly? Let me explain you by breaking down this process into 3 steps.

1. Convert your existing data into vector embeddings and store them in a database. Generally for this purpose, we use vector databases like Pinecone, Chroma etc.
    
2. Use the same embedding model that you used in step 1 to convert user's query to vector.
    
3. **Compare** user's query with the vectors present in your database and retrieve the ones that match the criteria the best.
    

To compare 2 vectors, there are several methods. We can either calculate the euclidian distance between the vectors and the ones that have the least distance between them are the most similar. We can also use dot product or cosine similarity to check how similar a pair of vectors are.

### Use Cases

As discussed above, vector embeddings work their magic under the hood of many applications ranging from search to AI chatbots. You can use different similarity techniques to utilise the power of embeddings in a vast variety of domains. Here are a few example:

**Recommendation System -** You can use the similarity algorithms to find entities that are similar to the ones that your user prefers.

**Semantic Search -** You can design search engines that not only match keywords but also use the meaning behind user's query to retrieve better results.

**Anomaly Detection -** You can also use similarity algorithms to detect anomalies amongst the data

**Question Answering Applications -** You can design applications that work on your custom data and answer user's queries based on the semantics rather than keywords.

And many more.

### Conclusion

In conclusion, vector embeddings represent a crucial advancement in natural language processing, enabling machines to move beyond keyword matching and grasp the intricate meanings and contexts within human language. As we continue to explore and refine these mathematical representations, the potential for innovation and improved AI applications becomes even more promising. The journey into the world of vector embeddings is one of continuous discovery and application, shaping the future of artificial intelligence.

That's a wrap! If you found this blog worth your time, or your learned something new, please do comment below :)

I write about AI, system design, software engineering, so if they interest you, make sure to follow me and subscribe to my Hashnode newsletter.

You can reach out to me at: [adityakrishna.com](https://adityakrishna.com)
