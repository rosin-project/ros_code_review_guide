# ROS Code Review Guide

Code review is having other members of a team critique software changes, and it is an important process for quality assurance. Traditional code review involved process mandates while modern code review is lightweight and flexible. ROS community adopted a lightweight code review process. This document covers the scope and high-level guideline for ROS code review. 

Code review is not an exact science or prescription, it is a subjective examination of the code to assess its internal quality. During this examination a critical and constructive evaluation of the code occurs. Various aspects of a code contribution should be evaluated: (1) Purpose, (2) Compliance with the coding standards and guidelines, (3) Architectural quality of the contribution, (4) Legibility of the code, (5) Maintainability of the code.

### Purpose:

1. Every contribution should have a purpose (i.e. New feature, bug fix, etc.). Does the submitted contribution accomplish a specific purpose? Is this purpose clearly documented?

### Compliance with the coding standards and guidelines:
1. Has the CI coding standards checker been run successfully?
1. Are any deviations from the coding standards justified and those justifications recorded?

### Architectural quality:
1. Is the proposed solution optimal and architecturally sound for the problem at hand? Think about how you would resolve the problem.
2. Try to identify shortcuts. Shortcuts may compromise maintaintability.
3. Modularity is an important feature to look for. It facilitates maintainability and ease of reading. Is the contribution modular? Can it be made modular?
4. Do proposed new features fit within the existing architecture?

### Legibility:

1. Is the code readability (the ease of reading and understanding the code) good? Use your code reading experience to judge the contribution's readability. Ask yourself, can I understand what the code does by reading it without needing to ask the original author? (i.e. [Developer Guide](https://github.com/ros2/ros2/wiki/Developer-Guide), [
ROS C++ Style Guide](http://wiki.ros.org/CppStyleGuide#Classes_.2BAC8_Types))
2. Consistency of the code style, naming conventions, but most importantly, consistency in architecture. i.e. Do the names (of fields, variables, parameters, methods and classes) actually reflect the concepts they represent?
3. Is the code sufficiently documented? Do you believe that the code is supported by adequate comments to enhance its readability and understanding? Use your own judgement and experience to assess the comments/code ratio.
4. Is the code over-commented? Overly verbose comments reduce readability.

### Maintainability:

1.	Is the contribution accompanied by appropriate test cases? Read the tests and check the coverage and the relevance. If there are no test cases, then raise it with the author of the contribution.
2.	Is the contribution accompanied by relevant documentation (i.e. README)? If there is existing documentation, then check whether it has been updated.
