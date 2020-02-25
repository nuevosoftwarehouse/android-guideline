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

class MainActivity: AppCompatActivity() { /*...*/ }

class ErrorDialog: Dialog() { /*...*/ }
```

## Function & Variables

Names of functions, properties and local variables start with a lower case letter and use the camel case and no underscores:

```kotlin
fun someFunctions() { /*...*/ }

var someVariable = 1
```

## Names for backing properties

If a class has two properties which are conceptually the same but one is part of a public API and another is an implementation detail, use an underscore as the prefix for the name of the private property:

```kotlin
class Foo {
    private val _elementList = mutableListOf<Element>()

    val elementList: List<Element>
         get() = _elementList
}
```

## Formatting

Use 4 spaces for indentation. Do not use tabs.

For curly braces, put the opening brace in the end of the line where the construct begins, and the closing brace on a separate line aligned horizontally with the opening construct.

```kotlin
if (elements != null) {
    for (element in elements) {
        // ...
    }
}
```

If the function signature doesn't fit on a single line, use the following syntax:

```kotlin
fun longMethodName(
    argument: ArgumentType = defaultValue,
    argument2: AnotherArgumentType
): ReturnType {
    // body
}
```

Prefer using an expression body for functions with the body consisting of a single expression.

```kotlin
fun foo(): Int {     // bad
    return 1
}

fun foo() = 1        // good
```
## Constants

Names of constants starts uppercase underscore-separated. Because many elements of Android SDK use a key-value pair approach,  names of the keys should be defined as const val with an appropriate prefixes.

| Element            | Field Name Prefix   |
| :----------------- | :------------------ |
| SharedPreferences  | `PREF_`             |
| Bundle             | `BUNDLE_`           |
| Fragment Arguments | `ARG_`        	   |
| Intent Extra       | `EXTRA_`            |
| Intent Action      | `ACTION_`           |

```kotlin
const val VALUE_MAX_LENGHT = 3
val KEY_USER_NAME = "UserName"

var someVariable: Int = 1

fun someMethod() { /*...*/ }

```

If it's needed to define several variables which is related to each other, they should use same prefix that indicates the relation.

```kotlin
const val ENDPOINT_API = "api"
const val PARAM_LANGUAGE = "lang"
const val PARAM_DATE = "date"
const val PARAM_SEARCH_QUERY = "search_query"
const val DURATION_MS_SESSION_TIMEOUT = 60 * 1000
const val DURATION_MS_OPENING_ANIMATION = 300
```

# License

```
Copyright 2020 Nuevo Softwarehouse.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
