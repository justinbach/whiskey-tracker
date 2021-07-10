# Overview

This is a toy project with two goals:
- nominally, to help users keep track of bottles in their whiskey collections, and
- actually, to serve as a playground for experimenting with a few different technologies

The application is simple, and should allow users to:
- log in with an identity provider
- register the purchase of a bottle of whiskey (distillery, bottle, batch, MSRP, actual purchase price)
- track tastings (date, quantity, tasting notes, rating)
- view their entire collection along with tasting notes
- search their collection

Proposed technologies and architectural choices:
- [Next.js](https://nextjs.org) for SSR and dynamic client-side functionality
- [Amazon S3](https://aws.amazon.com/s3/) to host static assets
- [Amazon Cognito](https://aws.amazon.com/cognito/) for user management
- [CQRS](https://martinfowler.com/bliki/CQRS.html) for separation of commands (acquisition of new bottles, recording tasting notes) and reads (collection and notes review, search)
- [Amazon API Gateway](https://aws.amazon.com/api-gateway/) to authorize and configure API requests
- [AWS Lambda](https://aws.amazon.com/lambda/) to handle API logic
- [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) as event store
- [AWS-managed Elasticsearch](https://aws.amazon.com/elasticsearch-service/) as searchable materialized view of collection
- [AWS CloudFormation](https://aws.amazon.com/cloudformation/) for management of cloud resources

# TODO

In rough order of priority:

- [ ] Create architecture diagram
- [ ] Add more tasks to this list :)