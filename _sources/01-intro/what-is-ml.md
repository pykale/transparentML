
## What is machine learning?

### Human learning

Learning is familiar to humans (and animals), as a continuous process that starts from birth and continues throughout life. A human child (and adult) learns new things, acquire new skills, and improve existing skills to survive and thrive in the surrounding world. A child's brain and senses perceive the facts of their surroundings to gradually learn the hidden patterns of life that help the child to craft logical rules to identify learned patterns and predict future events.

Learning is a process of acquiring new knowledge, skills, and behaviors. Learning can be divided into two categories: **acquisition** and **performance**. Acquisition is the process of acquiring new knowledge, skills, and behaviors. Performance is the process of using the acquired knowledge, skills, and behaviors to achieve a goal. Learning can be defined as a change in behavior or knowledge that results from experience. We learn from our experiences and we learn from others. For example, we learn to walk by watching others walk, we learn to speak by listening to others speak, we learn to drive by watching others drive, and we learn to cook by watching others cook.

You may have already known, since you are here, that machine can also learn, from their experiences, and from others. That is the subject of this course.

### A definition of machine learning

> Machine learning learns a model from data.

Machine learning takes **data** as **input** to learn a **model**, a mathematical representation of the data. This learning process is called the **training** phase and the data used in training is called the **training data**. After training, the learned model can take new data, the **test data**, as input to generate **output** for making predictions on the test data or for exploring/explaining the test data, which is the **test** phase.

The above definition is the one we will use in this course for clarity, loosely inspired by how the human brain learns certain things based on the data it perceives from the outside world. From this definition, we can see machine learning as a set of **software** tools for **modelling** and **understanding** complex **datasets**. You may find various definitions of machine learning elsewhere. For example, machine learning, from a systems perspective, is defined as the creation of automated systems that can learn hidden patterns from data to aid in making intelligent decisions.


### AI, machine learning, and deep learning

Besides machine learning (ML), you may have also heard about artificial intelligence (AI), deep learning, and data science. Some use these terms interchangeably, but they are not the same, as shown in the figure below.

```{figure} https://github.com/microsoft/ML-For-Beginners/raw/main/1-Introduction/1-intro-to-ML/images/ai-ml-ds.png
---
height: 250px
name: fig-ai-ml-ds
---
The relationships between AI, ML, deep learning, and data science, by [Jen Looper](https://twitter.com/jenlooper) adapted from [stackexchange](https://softwareengineering.stackexchange.com/questions/366996/distinction-between-ai-ml-neural-networks-deep-learning-and-data-mining) (can be redrawn by us later).
```

**AI** is a broad field of study that aims to create intelligent machines that can perform tasks that normally require human intelligence. There are multiple ways to achieve AI, and machine learning is one of them. As defined above, machine learning is a subfield of AI that machines acquire their experiences from data, in the form of a mathematical model. There are multiple ways of machine learning, and deep learning is one of them. **Deep learning** is a subfield of machine learning that uses deep (i.e. many layers) neural networks to learn from data. **Data science** is a broad field of study that uses scientific methods, processes, algorithms, and systems to extract knowledge and insights from data, not necessarily in the form of a mathematical model as machine learning does.
