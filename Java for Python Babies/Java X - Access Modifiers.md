# Java X - Access Modifiers

Access modifiers determine what can't and cannot (the scope) read or call properties or methods of a given class.

Below is a list of all major access modifiers

| Modifier    | Effect                                                         | Notes |
| ----------- | -------------------------------------------------------------- | ----- |
| `private`   | Can only be seen by methods within the class                   |       |
| `public`    | Can be seen anywhere                                           |       |
| `protected` | Can be seen only by methods within its class an any subclasses |       |

Additionally, the following keywords can be used to affect the scope

| Keyword  | Effect                                             | Notes                             |
| -------- | -------------------------------------------------- | --------------------------------- |
| `static` | Can be accessed **without initialising the class** | can be used with any of the above |
| `final`  | Cannot be overriden or changed                     | can be used with any of the above |
