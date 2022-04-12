# Read 14 - Event Driven Architecture

## Reading Material

[AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)

## Summary Notes

### AWS: SNS vs SQS

What is SNS and SQS?

- SNS = Simple Notification Service
  - Publisher-subscriber system
  - Many subscribers can receive the same message (fan-out approach)
  - These subscribers can be Lambda functions, a SQL endpoint, even an email server/user.
  - This works best when other systems care about an event.
- SQS = Simple Queue Service
  - Queuing service for message process
  - A system must poll the queue to keep up with events
  - A single consumer/service is the typical consumers for an event, with separate queues existing for separate consumers
  - This works best when your system cares about an event.

### An Example: Using SNS and SQS together to process credit card transactions

- In this example, you host an e-commerce site, and you're handling credit card transactions.
  - The transactions will be pre-processed by a transaction processor and validated by a credit card authority service
- The transaction processor passes off the payload to your application.
  - An SNS would be the optimal receiver for this payload, since it can fan it out to other services within your app, such as:
    - A Lambda function can send off an email to the customer thanking them for their purchase
    - An Analytics Queue stores the transaction for use by an Analytics service
    - A Fraud Detection Queue stores the transaction for use by a Fraud detection service.
