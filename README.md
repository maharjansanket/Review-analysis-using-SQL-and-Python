# Analyzing User Engagement and Success Metrics for Restaurants

## Agenda
1. Problem Statement
2. Analysis Objectives
3. Hypothesis
4. Data Overview
5. Analysis and Findings
6. Recommendations

<div align = "justify">

## Problem Statement
Analyzing User Engagement and Success Metrics for Restaurants

**Background:** The competitive restaurant industry needs understanding of customer engagement and success metrics. The metrices are crucial for restaurants to thrive. The analysis involves examining various aspects of user engagement, such as review counts, tip counts, check-ins, sentiment analysis, and correlating them with success metrics like average ratings, review count and business popularity.

## Objective

The primary goal is to analyze and understand user engagement patterns and their correlation with success metrics for restaurants. This analysis aims to provide actionable insights for restaurant owners and stakeholders to enhance customer experience, improve ratings, and drive business growth.


## Hypothesis

1. Higher levels of user engagement correlate with higher review and ratings for restaurants
The restaurants experiencing more user engagement, such as frequent reviews, tips, and check-ins, are likely to have higher overall ratings. Engaged users often indicate a strong interest in a restaurant, and their positive experiences are often reflected in higher ratings and reviews. Conversely, restaurants with lower engagement levels may struggle to attract attention and may have comparatively lower ratings.

2. Positive sentiment expressed in reviews and tips contributes top higher overall ratings and review counts for restaurants.
The positive sentiment expressed in user reviews and tips plays a crucial role in determining a restaurant's success metrics. Restaurants that consistently receive positive feedback in their reviews and tips are likely to have higher overall ratings and attract more reviews over time. Positive sentiments not only reflect customer satisfaction but also influence potential customers positively, leading to increased patronage and higher engagement levels.

3. Consistent engagement overtime is positively associated with sustained business success for restaurants
This hypothesis emphasizes the importance of consistent and sustained user engagement for long-term business success. Restaurants that maintain steady levels of engagement, such as regular reviews, tips, and check-ins, are more likely to sustain high ratings and review counts over time. Consistent positive interactions with customers build trust, loyalty, and a positive brand image, which are vital for ensuring sustained success in a competitive restaurant industry.

##Data Overview

Yelp is a popular online platform that provides crowd-sourced reviews about businesses, primarily restaurants but also including other local services like shopping, beauty, and entertainment. 

- The dataset used here is a subset of “Yelp” and has information about business across 8 metropolitan areas of US and Canada.
- It has 5 json files namely, business, review, user, tip and checkin.
- The json files are stored in the database for easy retrieval of data.
- Data Source: https://www.yelp.com/dataset

## Analyzing Steps

**1. User Engagement Analysis:**
Analyze review counts, tip counts, and check-in counts over time to identify peak engagement hours and days.
Explore seasonal trends or patterns in user engagement to understand customer behavior.

**2. Success Metrics Analysis:**
Calculate success metrics such as average ratings and popularity scores based on review and tip data.
Segment restaurants into high-rated and low-rated categories based on average ratings.

**3. Correlation Analysis:**
Investigate correlations between user engagement metrics (review counts, tip counts) and success metrics (average ratings, popularity).
Determine if there are any significant relationships between customer sentiments (from reviews and tips) and success metrics.

**4. Time Series Analysis:**
Visualize user engagement metrics (reviews, tips, check-ins) over time to identify busy hours or days for restaurants.
Identify any seasonal trends or recurring patterns in customer engagement.

**5. Comparative Analysis:**
Compare user engagement metrics between high-rated and low-rated restaurants to understand differences in customer interactions.
Analyze sentiment scores from reviews and tips to see if they align with success metrics or customer engagement patterns.

**6. Business Impact:**
Provide actionable insights and recommendations based on the analysis to improve customer experience, boost ratings, and enhance overall business performance.
Help stakeholders make informed decisions regarding marketing strategies, operational hours, and customer engagement initiatives.

**Key Deliverables:**
- Detailed analysis reports outlining findings, trends, and correlations discovered during the analysis.
- Visualizations including bar charts, heatmaps, and time series plots to support the analysis and insights.
- Recommendations and actionable insights tailored for restaurant owners and management teams to drive business growth and customer satisfaction.

## Analysis and Findings

### 1. Background
- The dataset has total of 150K business, out of which 35K are restaurants which are open.
- The tables shows the distribution of business success metrics (review count and average ratings)
  
![Screenshot 2024-05-13 at 17 48 28](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/6fb933b6-3138-4e0c-93b5-233a78411687)
![Screenshot 2024-05-13 at 17 49 33](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/4721b555-8353-4b38-ba79-92524fe232be)
![Screenshot 2024-05-13 at 17 51 43](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/23112fb0-a6a9-4ea4-9e99-5ae7fe382b56)

### 2. Highest Review Count VS Highest Rating

**1. Higher ratings do not guarantee a higher review count, or vice versa.**
A restaurant might have a high rating due to a smaller number of very positive reviews, while another might have a large number of reviews with mixed ratings. The number of reviews reflects the volume of feedback, but it doesn't necessarily correlate with the overall rating. Some highly rated restaurants might be less popular or newer, resulting in fewer reviews, whereas well-established or widely-known restaurants might accumulate more reviews over time, regardless of whether they are positive or negative.

**2. Success of Restaurants is not solely determined by rating or review counts.**
While ratings and review counts are important indicators of customer feedback and engagement, they are not the only metrics that determine a restaurant's success. Other factors such as location, quality of service, menu diversity, pricing, ambiance, marketing strategies, and even social media presence play crucial roles in a restaurant’s overall performance. High ratings and a substantial number of reviews can attract more customers, but consistent business success depends on a combination of various operational and strategic elements.

**3. Review count reflects user engagement but not necessarily overall customer satisfaction or business performance.**
A high review count indicates that a restaurant engages a large number of customers who are willing to share their experiences. However, it doesn't always equate to high customer satisfaction or strong business performance. The content and sentiment of the reviews are essential to understand the true customer satisfaction level. A restaurant might have numerous reviews, but if the sentiment is mostly negative, it indicates issues that could affect long-term performance. Conversely, a restaurant with fewer but consistently positive reviews might have high customer satisfaction and steady business performance.

![Screenshot 2024-05-13 at 17 51 43](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/e10368f6-026a-4327-9444-8a659cff1c4a)
![Screenshot 2024-05-13 at 17 53 41](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/aef55bb2-987d-43b6-9486-3e2eb9f18199)


### 3. Does higher engagement mean higher ratings?

Analysis of the dataset reveals a positive correlation between a restaurant's star rating and its engagement metrics, such as the number of reviews and check-ins. As restaurants improve their ratings from 1 star to 4 stars, there is a notable increase in the average number of reviews and check-ins. This trend suggests that higher-rated restaurants tend to attract more customer interactions, indicating a broader customer base and increased visibility.

Restaurants with a 4-star rating show the peak of user engagement, marked by the highest counts of reviews and check-ins. This level of rating seems to hit the sweet spot for attracting a large number of customers willing to engage. However, as the ratings increase above 4 stars, there is a noticeable decline in engagement metrics. This downward trend might indicate that while very high ratings are desirable, they do not necessarily lead to increased customer interactions.

The reduction in engagement for restaurants with perfect 5-star ratings could be attributed to a few factors. One possibility is a saturation effect, where customers see a perfect score and feel that their additional positive feedback is unnecessary. Alternatively, these establishments might attract a highly selective group of patrons who are consistently satisfied, resulting in fewer but uniformly positive reviews. This selectivity could mean that while these restaurants maintain exceptional standards, their customer base is smaller and more niche.

![Screenshot 2024-05-13 at 17 56 14](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/597a5bbf-e738-4b5d-97f9-3ff0d8191029)

### 4. Is there a correlation between number of reviews, tips and check-ins?

The analysis of the dataset shows that user engagement metrics such as reviews, tips, and check-ins are closely connected. For instance, businesses that receive a high number of reviews also tend to have more check-ins and tips. This interconnection implies that active customer participation in one form of engagement often correlates with increased activity in other forms. Essentially, if customers are engaged enough to leave a review, they are likely to engage in other ways, such as checking in or leaving tips, creating a comprehensive pattern of high engagement across multiple interaction points.

Given the interlinked nature of user engagement metrics, businesses can benefit from adopting holistic strategies that encourage multiple forms of customer interaction. By fostering an environment where customers are motivated to leave reviews, check in, and give tips, businesses can amplify their overall engagement levels. For example, initiatives such as loyalty programs, special events, or customer appreciation incentives can stimulate diverse forms of participation. These activities not only increase direct engagement but also enhance the business's visibility and attractiveness to potential new customers, leading to sustained growth and success.

![Screenshot 2024-05-13 at 17 57 48](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/f2606ab1-58a3-4093-820a-1ffed827ce48)



### 5. How do the success metrics of restaurant vary in different states and cities?

Philadelphia stands out as the leading city in terms of restaurant success, which is measured by a composite score that includes both high average ratings and substantial user engagement across various metrics like reviews, tips, and check-ins. This indicates that restaurants in Philadelphia not only receive high ratings from their patrons but also experience a high level of interaction and activity from their customers. The combination of high ratings and active engagement suggests a vibrant and satisfied customer base, which is a strong indicator of the health and popularity of the restaurant industry in Philadelphia.

After Philadelphia, cities like Tampa, Indianapolis, and Tucson also show significant success scores. This suggests that these cities have restaurant scenes that are thriving and robust. The high success scores in these areas imply that restaurants are not only well-rated by their customers but also enjoy active user engagement. This could be due to a variety of factors such as diverse culinary offerings, effective customer service, and successful marketing strategies that encourage customers to interact more with the businesses. The high engagement and ratings reflect strong local support and a dynamic food culture in these cities, highlighting their importance as key culinary destinations.
![Screenshot 2024-05-13 at 18 02 03](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/363c227b-cd73-4782-96a8-ba05ce704330)


### 6. Are there any patterns in user engagement over time fo rth esuccessful business compared to the less successful ones?

Businesses that are deemed successful—specifically those with ratings of 3.5 stars or higher—demonstrate a pattern of consistent, and in some cases, increasing user engagement over time. This engagement includes metrics such as reviews, tips, and check-ins, all of which indicate that customers are regularly interacting with these businesses. The steady or upward trend in user engagement suggests that these businesses are not only meeting but often exceeding customer expectations, leading to sustained customer interest and loyalty. This continuous interaction can be attributed to a combination of high-quality service, effective customer relationship management, and possibly innovative marketing strategies that keep customers engaged and coming back.

High-rated restaurants, those that consistently achieve ratings above 3.5 stars, manage to sustain or even grow their levels of user engagement over extended periods. This sustained engagement is a strong indicator of ongoing customer satisfaction and interest. When customers frequently leave reviews, give tips, and check-in at these establishments, it highlights that they are not only visiting these restaurants but are also motivated to share their positive experiences. This ongoing interaction is crucial for the restaurants as it helps in maintaining a high profile and attracting new customers, further reinforcing their success. The ability to maintain or increase engagement over time shows that these restaurants are effectively meeting customer needs and adapting to changes in customer preferences and market trends.

![Screenshot 2024-05-13 at 18 02 25](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/812f9bdc-44ee-4b8c-91ea-b4a3c9f117ab)

### 7. Trend and seasonality

High Engagement Periods (November to March):** The analysis indicates that the months from November to March exhibit significantly higher levels of user engagement for restaurants. This period sees increased activity in terms of reviews, tips, and check-ins.

This trend can be attributed to several factors such as holiday seasons (Thanksgiving, Christmas, New Year), winter holidays, and indoor dining preferences during colder months. These times of the year often encourage more social gatherings and dining out, leading to higher engagement on platforms like Yelp.

By understanding these seasonal engagement trends, restaurant owners can strategically plan their marketing campaigns, special promotions, and staffing schedules to capitalize on these peak periods of user activity.

![Screenshot 2024-05-13 at 18 03 09](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/456d4de4-c89d-46e7-a11e-665f0c01a6d3)
![Screenshot 2024-05-13 at 18 03 27](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/3f139a0d-41ac-4707-8a2a-1334f323ed01)

### How does the sentiment of reviews and tips correlate with the success metrics of restaurants?

In the context of Yelp reviews, users can provide additional feedback on individual reviews by marking them as "Useful", "Funny", or "Cool". These attributes help other users to gauge the quality and relevance of a review beyond just the star rating. A "Useful" review might provide detailed, practical information that helps potential customers make informed decisions. A "Funny" review adds a touch of humor, making it more enjoyable to read and often more memorable. A "Cool" review typically denotes a certain level of creativity or uniqueness that stands out. These attributes collectively enhance the richness of the feedback ecosystem on Yelp, providing more nuanced insights into user experiences.

When a restaurant's reviews frequently receive "Useful", "Funny", or "Cool" feedback, it indicates that customers are not only engaging with the reviews but also finding them valuable and enjoyable. High counts of these attributes suggest that the restaurant is fostering a positive, interactive community where customers feel compelled to share their experiences and acknowledge the contributions of others. This level of engagement is a strong indicator of customer satisfaction and loyalty. It reflects that the restaurant is consistently delivering experiences that resonate well with its patrons, thereby encouraging them to return and recommend the place to others. Consequently, this ongoing positive feedback loop plays a crucial role in the restaurant's overall success, helping to attract new customers and retain existing ones.

![Screenshot 2024-05-13 at 18 04 01](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/145d4146-5b0e-4771-ae52-ecd3dab13683)


### Is there any difference in engagement of elite users and non-elite users?

Yelp's Elite status is granted to users who consistently contribute high-quality reviews, photos, and other content to the platform. These users are often considered experts or enthusiasts in their local communities, known for their detailed and helpful reviews, insightful photos, and active engagement with other users and businesses. Achieving Elite status signifies a level of trust and credibility within the Yelp community, making their opinions and recommendations influential among other users.

Although Elite users represent a smaller percentage of the overall Yelp user base, their impact on the platform's content and engagement metrics is significant. Elite users tend to write more reviews, provide detailed feedback, upload high-quality photos, and actively participate in discussions and events. As a result, their contributions contribute disproportionately to the total review count and overall engagement metrics on Yelp. Their reviews often carry more weight due to their status and reputation within the community.

Since Elite users are typically passionate about exploring and reviewing local businesses, building a positive rapport with them can have long-term benefits for restaurants and other establishments. Elite users are more inclined to revisit and recommend businesses where they have positive experiences. They often have a loyal following among other Yelp users who trust their recommendations. Therefore, businesses that prioritize providing excellent service and experiences to Elite users not only benefit from their direct reviews and feedback but also from the influence they wield in shaping opinions and driving customer loyalty within their social circles and the broader Yelp community.

![Screenshot 2024-05-13 at 18 04 32](https://github.com/maharjansanket/Review-analysis-using-SQL-and-Python/assets/25703361/5a81d35e-f320-4515-ba0f-396f258e272a)


</div>


