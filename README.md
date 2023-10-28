# mock-java
Simple Jest like Mocking framework for Java/Android

## How to use
The Mock class provides methods for tracking calls and then later asserting that they were called as you were expecting. The method names were inspired by the popular JavaScript testing framework Jest.
To get started, extend the Mock class and add calls to addCall() in your mocked functions to begin tracking calls.

You can then use the following functions to assert whether a function was called as expected.

### toHaveBeenCalled(String method)
Check whether the call stack of the class contains a call to the provided method name

### toHaveBeenCalledWith(String method, Object... arguments)
Check whether the call stack of the class contains a call to the provided method name with the provided arguments (if any)

### toHaveBeenCalledExactly(String method, int times)
Check whether the call stack contains exactly the number of calls to the provided method name

### toHaveBeenCalledExacltyWith(String method, int times, Object... arguments)
Check whether the call stack contains exactly the number of calls to the provided method name with the provided arguments (if any)

### toHaveBeenCalledAtLeast(String method, int min)
Check whether the call stack contains at least min calls to the provided method name

### toHaveBeenCalledAtLeastWith(String method, int min, Object... arguments)
Check whether the call stack contains at least min calls to the provided method name with the provided arguments (if any)

### lastCalledWith(String method, Object... arguments)
Check whether the last entry on the call stack for the given function name was with the provided arguments (if any)

## Additional useful functions

### reset()
Clear the recorded call stack, resetting the mock

### getCalls()
Retrieve the call stack for the Mock class

### addCall(String method, Object... arguments)
Record a call to the given function name with the given arguments (if any).
The method name here must exactly match the name provided to the assertion functions to properly match the calls. For best results use the method name themselves.
