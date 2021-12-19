# Docomo code Excercise
## Context
Cucumber and Rest-Assured maven based automation framework to test an application that is a payment gateway which allows merchants to charge their users with a single integration.The framework from start is expecting the gate way appliaction to be running on the following port http://localhost:8088 

## Requirements
1. JAVA 8
2. MAVEN
3. GIT

## Test cases been tested
1.API should expose the following endpoint POST /operations/{id}/refund

2.The "id" should be a valid uuid v4 (ex. d1e90d8f-11f7-41e0-92ff-235e2a85ab3b) to get 201 OK

3.With an invalid uuid you should get a 400

4.Only one concurrent refund operation (on the same transaction id) can be performed, so the resource should be blocked if another refund is being processed. Failing concurrencies should get a 423
