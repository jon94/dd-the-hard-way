# dd-the-hard-way

## How to use this?
Read this section before continuing. 
- Clone this repo.
- There are no right or wrong answers as there are many ways to achieve the same outcome.
- Along the exercise, there will be questions designed to make you think harder about certain fundamental concepts.

## Intent of Exercise
- Hands on Exercise aiming to help you understand key fundamentals of Datadog Platform
- Feel free to mark sections as done after you have fully understood it.
    - *Infrastructure*
    - [ ] Agent Metrics (What metrics come from the agent installation? Why install the agent?)
    - [ ] Agent Tags (Which telemetry will tags propagate to?)
    - [ ] Collect Processes (What exactly are these processes?)
    - *Logs* 
    - [ ] Tail files using agent on host
    - [ ] Tail files using containerized agent (Try to understand what you have to do in order to achieve this)
    - *APM*
    - [ ] APM Trace Metrics (Why is this important to mention? How are these generated?)
    - [ ] APM Runtime Metrics (How are these being generated without Datadog APM? How are these generated with Datadog APM?)
    - [ ] If 10 successful requests with HTTP 200OK response are sent to your backend instrumented with APM, will you see all 10 requests in the Trace Explorer?

## Exercise
- If you have access to AWS Sandbox on Datadog
  - Spin up EC2 Machine using AMI (java-docker) in region ap-south-1
  - Else just spin up a VM, install java and docker yourself.

### Part 1: Host Level Familiarization   
- *Task 1: Setting up the Application on VM*
- [ ] Using the provided [.jar file](https://github.com/stackify/example-apps/raw/main/sample-java-petclinic/spring-petclinic-2.7.0.jar), your goal is to make sure you can access the application on the public IP of the VM that you have spun up earlier. Aim to run the Java Process in the background.
- [ ] What is the PID of the java process that is running on the host?

- *Task 2: Infra - Installing the Datadog Agent in the VM*
- [ ] Using your provided Datadog sandbox account, install the latest Datadog Agent into the VM.
- [ ] Add tags as part of the set up. env:challenge, team:sales-eng
  - Think about tags and where it is being propagated.
- [ ] Where can you find the PID of the java process in the datadog platform?
- [ ] What metrics are collected by the agent? 

- *Task 3: Logs - Use the Datadog Agent to collect Logs*
- [ ] Collect application logs related to the Java App

- *Task 4: APM - Instrument the .jar file using dd-trace-java APM SDK*
- [ ] Instrument the Java App using the Datadog Tracer, do not use Single Step Instrumentation
- [ ] Set up Trace Log Correlation
- [ ] Other than Spans, what other information does APM give?
- [ ] What is the purpose of Unified Service Tagging? If you have not done so, try setting it up.

- *Task 5: APM - Instrument the .jar file using Single Step Instrumentation*
- [ ] Revert what you have done in Task 4 and try instrumenting the Java App using Single Step Instrumentation.
- [ ] What is the difference now? When and why do you think we should use Single Step Instrumentation?
- [ ] What are some potential limitations for SSI today?

### Part 2: Container Level Familiarization
