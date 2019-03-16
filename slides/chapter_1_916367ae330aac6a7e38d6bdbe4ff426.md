---
title: Insert title here
key: 916367ae330aac6a7e38d6bdbe4ff426

---
## Lesson 1:  Introduction to Data Engineering

```yaml
type: "TitleSlide"
key: "27391da623"
```

`@lower_third`

name: Robert Chang
title: Data Scientist


`@script`



---
## The Evolution of Analytics Capability

```yaml
type: "FullSlide"
key: "d5e156f124"
```

`@part1`
![image](https://cdn-images-1.medium.com/max/1600/1*7IMev5xslc9FLxr9hHhpFw.png)


`@script`
Have you heard of Abraham Maslow's famous Hierarchy of Needs? In this theory, he laid out the progression of human needs, and argued that in order for the motivation for the next level to occur, the previous level of needs must be satisfied first before moving on to the next.

In 2017, Monica Rogati, an early LinkedIn data scientist, coined the term "The Data Science Hierarchy of Needs", where she argued that analytics capabilities are built layers upon layers, and just like Maslow's theory, one cannot move to the next stage of analytics until the foundation has been built. 

So what are the layers? The triangle chart below shows you the steps a typical company needs to go through to transform itself from a great company to a great data-driven company. 

First, at the bottommost layer, we need to start by building the infrastructure to collect data, such as logging and instrumentation. We will discuss the concept of instrumentation in details in later exercise, but think of it as a mechanism to understand how user interacts with the product (e.g. impression, clicks, page bounce, and more).

Once the raw data is stored, we need to move and and store these raw data in a secure place so we can use them in the future. In later chapter, we will talked about some of the most popular cloud service providers to explain how data is stored in modern data data-driven companies.

Going to the next level, we need to transform and clean the raw data in order to make them more usable. In later chapter, we will discuss the concept of ETL (Extract, Transform, and Load), which is a core concept for building a data warehouse.

With all this hard work, we can then finally start doing higher-valued work such as analytics, metrics tracking, and building dashboards. Beyond that, mature data-driven companies also use the same data to build experimentation platform to perform A/B test, or use them to construct training data for Machine Learning Model.

Unfortunately, in most of the news article out there nowadays, there is a strong emphasis on work that is happening in the top of the pyramid, rather than all the other foundational work that are less glamorous. However, it is important to have this mental model in mind. Without the foundation, analytics is not possible.


---
## BackTracking: From Tables To Warehouse

```yaml
type: "TwoColumns"
key: "f63e9c7f7e"
```

`@part1`
```sql
SELECT
	*
FROM
	magical_table
WHERE
	ds = '{{ ds }}'
```


`@part2`
![image](https://cdn-images-1.medium.com/max/2000/1*tcDY4JKmvgfR0x_x0gpS_Q.png)


`@script`
Most of you probably have the experience performing data analysis by manipulating data from a excel spreadsheet or querying from a SQL table, but have you ever wonder where these tables came from?

Data Tables (like the ones on the left) typically do not magically appeared themselves. There are a lot of work that needs to happen for table to be cleaned, transformed, and make usable, as we have already mentioned in the previous slide "The Data Science Hierarchy of Needs". 

But what exactly is the kind of work to goes into Data Engineering? In the later chapters, we will dive deep into various activities related to Data Engineering, but it is useful to start with the big picture so we can understand the mental model of Data Engineering.

First of all, we need to collect data, and data can come from a wide variety of data sourcs, such as production database exports, user-initiated logs, and even just .csv files. 

With all the data collected, we need to store them in a secure place where we can reuse them, this is what we often call "the data warehouse", a term that was coined in the 1970s by Computer Scientist Bill Inmon.

However, we do not want to dump raw data into the warehouse, because they are not very useful. As a result, between transferring raw data to usable data to the data warehouse, we need to clean, transform, and massage the data - this process is what we called ETL - extract, transform, and load. A big part of Data Engineering is about how to do ETL at scale with best practices. 

Finally, once the data is stored in the data warehouse, it can then be used for a variety of purposes: 

For example, useful tables that keep track of key business metrics can be used for business intelligence of dashboards.

Similarly, logging of users actions, when overlay with experiment assignment data, can be used to automatically calculate user engagement statistics between control and treatment group. All this can be used to build an experimentation platform. 

Last but not least, the same data can be used to construct a training set that will be used to trained a Machine Learning Model.

A big challenge of data-driven company is how to organize such data warehouse so the same data can be applied to a wide variety of different use cases.


---
## Let's practice!

```yaml
type: "FinalSlide"
key: "b236d6b355"
```

`@script`


