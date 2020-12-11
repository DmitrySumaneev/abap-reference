# Functions

## Purpose

This provides tips on working with functions and function groups.

## Contents

- [How to](#how-to)
  - [How to copy a function group](#how-to-copy-a-function-group)
  - [How to call a function in remote system and don't wait for a response](#how-to-call-a-function-in-remote-system-and-dont-wait-for-a-response)

### How to copy a function group

To copy a function group you can use Transaction **SE38**. Put the name of the function group in the Name field and add *"SAPL"* at th begginning:

```ABAP
    SAPLZ_MY_FUNCTION_GROUP.
```

### How to call a function in remote system and don't wait for a response

Use [Asynchronous function call](https://help.sap.com/viewer/753088fc00704d0a80e7fbd6803c8adb/7.5.19/en-US/4889673284b84e6fe10000000a421937.html).
