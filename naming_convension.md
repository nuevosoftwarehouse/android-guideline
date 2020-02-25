# Naming convention
Inspired by official [Kotlin conventions](https://kotlinlang.org/docs/reference/coding-conventions.html#naming-rules)

## Packages
The package name is used for unique identification for your application. Names of packages are always lower case and do not use underscores.    
| Good           			  | Bad   				         |
| :-------------------------- | :--------------------------- |
| `com.nuevo.project` 		  | `com.nuevo.Project` 		 |
| `com.nuevo.awesomeproject` | `com.nuevo.awesome_project` |

## Classes

Names of classes and objects start with an upper case letter and use the camel case:

```kotlin
data class SomeDataClass { /*...*/ }

class SplashActivity: AppCompatActivity() { /*...*/ }

class LoginErrorDialog: Dialog() { /*...*/ }
```

## Function names

Names of functions, properties and local variables start with a lower case letter and use the camel case and no underscores:

```kotlin

fun someFunctions() { /*...*/ }

var someVariable = 1
```