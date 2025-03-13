# Assignment: Black Box Testing of the "SmartLock" System

**Objective:**

* To perform black box testing on a provided compiled library (`SmartLock.dll` or `smartlock.jar`).
* To discover and document the system's behavior through testing.
* To identify and analyze a hidden, randomly triggered error within the system.
* To automate the test execution using GitHub Actions.

**System Description:**

### C#
You are provided with a compiled C# DLL, "leetgrind.dll," containing an obfuscated implementation of a smart lock system. The system provides the following public methods:

* `Reset()`: Resets the lock to its initial state.
* `EnterCode(string code)`: Attempts to unlock the lock with the provided code.
* `Lock()`: Locks the lock.
* `GetLockState()`: Returns the current state of the lock.

### Java 2
You are provided with a compiled JDK jar, "lock.jar," containing an obfuscated implementation of a smart lock system. The system provides the following public methods:

* `reset()`: Resets the lock to its initial state.
* `enterCode(string code)`: Attempts to unlock the lock with the provided code.
* `lock()`: Locks the lock.
* `getLockState()`: Returns the current state of the lock.

**Tasks:**

1.  **DLL/JAR Integration:**
    * Create a test application (in any language that can interact with a DLL) to utilize the "leetgrind.dll.". The DLL is compiled using `DotNet 8.0`
    * If you are using Java create an application in any language that can interact with JAR. The JAR is compiled using `JDK 21.0.6`
2.  **State Transition Analysis:**
    * Analyze the behavior of the lock system by interacting with its public methods.
    * Create a state transition diagram that represents the observed behavior of the lock system.
3.  **Test Case Design:**
    * Design black box test cases to test the lock.
    * Include test cases for:
        * Valid and invalid code inputs.
        * State transitions between "Locked," "Unlocked," and "Fault" states.
        * Boundary conditions and edge cases.
        * Testing the `Reset()` and `Lock()` methods.
4.  **Error Discovery and Analysis:**
    * Through testing, discover the hidden, randomly triggered error within the `EnterCode()` method.
    * Analyze the conditions that trigger the error, including:
        * The probability of the error occurring.
        * Any patterns or dependencies related to the error.
        * The exact number of incorrect password attempts that triggers the lock to go into an error state.

5.  **Test Reporting:**

    * Prepare a test report (ONLY PDF or Gihub Markdown format) that includes:
        * A state transition diagram.
        * An analysis of the discovered random error
        * Recommendations for any improvements

6. **Test Automation with GitHub Actions:**
     * Create a GitHub repository for your test project.
        * Implement a GitHub Actions workflow that: 
        * Executes your test cases. 
        * Ensure that the workflow passes successfully.

**Note**:
The PDF/Github markdown of your report should be uploaded on Github.

**Bonus:**

* Successfully determine the exact number of attemps and probablity that can cause the lock to enter the "Fault" state.

**Evaluation Criteria:**

* Completeness and effectiveness of test cases.
* Accuracy of state transition analysis.
* Thoroughness of error discovery and analysis.
* Clarity and completeness of the test report.

**Important Notes:**

* You are not allowed to modify the provided "SmartLock.dll."
* Focus on black box testing techniques to discover the system's behavior.
* Pay close attention to boundary conditions and edge cases.
