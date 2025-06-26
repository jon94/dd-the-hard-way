# dd-the-hard-way

## How to use this?
Read this section before continuing. 
- Clone this repo.
- There are no right or wrong answers as there are many ways to achieve the same outcome.
- Along the exercise, there will be questions designed to make you think harder about certain fundamental concepts.

## Intent of Exercise
- Hands on Exercise aiming to help you understand key fundamentals of Datadog Platform
- Feel free to mark sections as done after you have fully understood it.
    - Infrastructure
    [] Agent Metrics (What metrics come from the agent installation? Why install the agent?)
    [] Agent Tags (Which telemetry will tags propagate to?)
    [] Collect Processes (What exactly are these processes?)
    - Logs 
    [] Tail files using agent on host
    [] Tail files using containerized agent (Try to understand what you have to do in order to achieve this)
    - APM
    [] APM Trace Metrics (Why is this important to mention? How are these generated?)
    [] APM Runtime Metrics (How are these being generated without Datadog APM? How are these generated with Datadog APM?)
    [] If 10 successful requests with HTTP 200OK response are sent to your backend instrumented with APM, will you see all 10 requests in the Trace Explorer?

## Exercise
- If you have access to AWS Sandbox on Datadog
  - Spin up EC2 Machine using AMI (java-docker) in region ap-south-1
- Task 1

