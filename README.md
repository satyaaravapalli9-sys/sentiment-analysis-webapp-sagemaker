# Sentiment Analysis Web-app using AWS SageMaker

A simple Web app for interacting with the Sentiment Analysis model using AWS SageMaker for the purpose of determining the sentiment of a movie review using the IMDB data set. 

![alt text](image.jpg)

The diagram above gives an overview of how the various services will work together. On the far right is the model which we trained is deployed using SageMaker. On the far left is our web app that collects a user's movie review, sends it off and expects a positive or negative sentiment in return.

In the middle is where some of the magic happens. We will construct a Lambda function, which we can think of as a straightforward Python function that can be executed whenever a specified event occurs. We will give this function permission to send and receive data from a SageMaker endpoint.

Lastly, the method we will use to execute the Lambda function is a new endpoint that we will create using API Gateway. This endpoint will be a URL that listens for data to be sent to it. Once it gets some data it will pass that data on to the Lambda function and then return whatever the Lambda function returns. Essentially it will act as an interface that lets our web app communicate with the Lambda function.

#### A Positive Review Example

![alt text](positive.gif)

#### A Negative Review Example

![alt text](negative.gif)

## Maintainer

**Satya Kumar**
Java Full Stack Developer | AWS | AI | SRE

Satya is a Java Full Stack Developer with over 5 years of experience building and supporting production systems using Java, Spring Boot, React, AWS, and Kubernetes. With a strong focus on microservices, distributed systems, and Site Reliability Engineering, he specializes in improving system stability, performance, and deployment reliability. This project demonstrates his hands-on experience with AWS cloud environments and AI-enabled workflows.

**Contact Information:**
- Email: satyaaravapalli9@gmail.com
- GitHub: https://github.com/
- LinkedIn: https://www.linkedin.com/