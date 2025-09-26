# Overview: A Data Management System

Your task is to define a service for managing course and module data and create a simple local implementation of that service.
For now, there is no remote API to communicate with but it will adhere to the provided JSON data specification.
It should be possible, in the future, to write an implementation for the remote API without modifications to the rest of the application.

# Project Setup & Submission

- Unity Version: Please use Unity 6000.0 LTS or a more recent version.
- Submission: Please upload your completed project to a private Git repository (GitHub, GitLab, etc.). Invite us to the repository and notify us via email when you're finished.

# Core Requirements (Must-Haves)

Your service must meet the following functional requirements:

- Write your service definition in the empty provided `IModuleService`.
- We should be able to create, retrieve, update and delete courses and modules.
- It should be possible to swap out the local implementation of the service to a new remote implementation with no modification to any code that depends on this service.
  - The only modifications that should be needed to swap the service is to instantiate and supply the new implementation.
  - It is not expected that you will write or use any dependency injection framework for this test, simply passing through dependencies is fine.
  - Please be prepared to demonstrate how we would change to a new implementation.
- Serialization format is JSON. Newtonsoft's library is already added to the project. Extensive knowledge of Newtonsoft's library shouldn't be needed but care will need to be taken over how enums are serialized.
- Course and module data should be initially populated with the default provided data.
- In the local implementation, changes to the course and module data should persist when the application is closed and relaunched. Where and how the data is stored is up to you.
- Consider defining your service methods as asynchronous (`Task<T>`) even for the local implementation, as the future remote API will require this.

# Bonus Goals (Optional Nice-to-Haves). 
These are not required. If you finish the core task and want to demonstrate additional skills, feel free to tackle one of these challenges.

- Some way to either manually or automatically test the service and implementation. This could be using Unity UI, an Editor window or automated tests.
- Decide on an approach to error and exception handling that can be carried forward to future service implementations.

# What We're Looking For

We’ll be reviewing your submission with a focus on these areas:

- Architecture: Have the must-have features been met by the architecture choices?
- C# Best Practices: Is the code clean, readable, and robust?
- Clarity & Documentation: Is your code easy to understand? A README.md file in your Git repo with a brief explanation of your design choices is highly encouraged.

# Final Notes

- Time Expectation: This test should take you about 2-3 hours. Please do not spend more than 4 hours on it. We respect your time and are interested in your best work within that timeframe.
- Original Work: The code should be your own. You're free to use online resources like the Unity documentation or Stack Overflow, just as you would in a daily work environment.
- AI tools: Use of AI is encouraged to make the most efficient use of your time. Please take care to properly understand, modify and fix any generated code.
- Deadline: Please submit your test within a week of receiving this email. If you need more time, just let us know.
