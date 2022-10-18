## Introduction to Solidity

#### Getter Functions
- View function declares that no state will be changed.

- Pure function declares that no state variable will be changed or read.


### Error handling
=> An error can be thrown by calling 
 - require ->  Validate inputs and condition before execution
 - assert -> is used to check for code that should never be false. Failing assertion probably means that there is a bug.
 - revert -> is similar to require. See the code below for details.
  
```js
contract Error {
    function testRequire(uint _i) public pure {
        require(_i > 10, "Input must be greater than 10");
    }

    function testRevert(uint _i) public pure {
      if (_i < 10) {
        revert("Index must be greater than 10");
      }
    }

}
```

> Assert should only be used for internal errors and for check constant numbers



