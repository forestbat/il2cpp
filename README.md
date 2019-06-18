il2cpp
===

> 「  With develop efficient of C#，run efficient of C++  」

![alt tag](https://github.com/anydream/il2cpp/raw/master/il2cpp-schematic.png)

## How to test
  - Pre-requirements:
    1. Windows 7 or later, 64-bit system;
    2. Visual Studio **2017**, C# and C++ desktop dev environments;
  - Open ``il2cpp.sln``;
  - Set ``test`` as startup project;
  - Run.
  - You can add your test code into ``CodeGenTests.cs`` like this:
    ```CSharp
    [CodeGen]
    static class MyTest
    {
        // return 0 means PASS, otherwise means FAIL
        public static int Entry()
        {
            int a = 1, b = 2;
            if (a + b != 3)
                return 1;
            return 0;
        }
    }
    ```
  - Run ``test`` project to test your code.


## Attributes released
- [x] Analysis for Class,Method and Field,extract the smallest dependencies
- [x] Callvirt and virtual table binding
- [x] Explicit overriding for interface and base class method
- [x] Contravariant/covariant analysis
- [x] Built-in conservative GC（It's bohem，I have removed）
- [x] Static constructor
- [x] Analysis and code generation of try/catch/finally/fault Exception code block
- [x] Code generation of 1-dim array and multi-dim array
- [x] Handle of Enum
- [x] Code generation of string const
- [x] Code generation of Nullable
- [x] Explicit field layout and struct length
- [x] Method delegate
- [x] C++ code compiler tools
- [x] Read/write commands of array
- [x] Stack operation commands
- [x] load const commands
- [x] method call commands
- [x] Read/Write commands for variable/parameters/field
- [x] Condition and branches commands
- [x] Compare commands
- [x] Number convert commands
- [x] Number calculate commands
- [x] Struct and Ref objects operation commands
- [x] Read/Write commands for pointer
- [x] Commands for handling exception
- [x] Box/unbox
- [x] Commands for overflow checking

## Not a goal
- [x] Create new type in run-time (TypeBuilder.CreateType)
- [x] Generate and run Emit/Expression Trees/Native code in run-time
- [x] Load .NET DLL and initialize its instance in run-time
- [x] Initialize generic expansions which aren't exist in compiling duration
- [x] Add/Delete/Edit reflection information in run-time
- [x] Recursion type parameter expansion 
- [x] Marshaling delegate of no-static methods
