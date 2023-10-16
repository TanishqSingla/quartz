**Difficulty in setting up realistic and useful tests**

> Writing realistic and useful test is a challenge with unit tests.  
> It is necessary to create relevant initial conditions so the part of the application being tested behaves like the part of the complete system. If these conditions are not set properly then the test won't be running the code in a realistic context, which diminishes the value and accuracy of unit test results.

**Requires discipline throughout the development process**

> To obtain the benefits from unit testing rigorous discipline is needed throughout the development process.

**Requires Version Control**

> Unit tests requires careful records of how the tests have been performed and the changes that have been made to them.

**Requires regular reviews**

> It is also essential to implement a sustainable process for ensuring that the test case failures are reviewed regularly and addressed immediately. If such a process is not implemented then the application will evolve out of sync with the unit test suite, increasing false positives and reducing effectiveness of the test suite.

**Limitations for embedded system software**

> Unit testing embedded system software presents a unique challenge: Because the software is being developed on a different platform than the one it will eventually run on, you cannot readily run a test program in the actual deployment environment, as is possible with desktop programs.

**Limitations for testing integrations with external systems**

> Unit tests tend to be easiest when a method has input parameters and some output.  
> It is not easy to create a unit tests when a major function of the method is to interact with something external to the application.