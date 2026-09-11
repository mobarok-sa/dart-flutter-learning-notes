# Dart Basics — Cheat Sheet


Course Link: https://www.educative.io/courses/learn-dart-first-step-to-flutter/a-bit-about-dart-vs-flutter



## 1. String Length

Use `.length` to find the number of characters in a string.

```dart
print('hello'.length);
```

**Output:**

```text
5
```

> `.length` returns the number of characters in the string.

---

## 2. Variables in Dart

A variable stores a value.

### Explicit Type

You can declare a variable by specifying its data type:

```dart
int number = 5;
```

Here:

* `int` → data type
* `number` → variable name
* `5` → value

---

## 3. Declaration and Assignment Separately

You can declare a variable first and assign a value later.

```dart
int number;

number = 6;
```

This is useful when you don't know the value at the time of declaration.

---

## 4. Type Inference

Modern Dart heavily uses **type inference**.

This means Dart can automatically determine the type of a variable from its value.

For example:

```dart
var age = 25;
```

Dart understands that `age` is an `int`.

You don't always need to write:

```dart
int age = 25;
```

You can simply write:

```dart
var age = 25;
```

---

# 5. `var`

`var` creates a variable whose value **can be changed/reassigned**.

```dart
var age = 25;

age = 30;
```

✅ Allowed:

```dart
var age = 25;
age = 30;
```

The variable can be reassigned, but its inferred type remains the same.

---

# 6. `final`

`final` creates a variable whose value can be **set only once**.

```dart
final name = 'Alice';
```

After assigning the value, you **cannot change it**.

❌ Not allowed:

```dart
final name = 'Alice';

name = 'Bob'; // Error
```

### Example

```dart
final name = 'Alice';

print(name);
```

Output:

```text
Alice
```

---

# 7. `var` vs `final`

| Keyword | Can reassign? | Example                 |
| ------- | ------------- | ----------------------- |
| `var`   | ✅ Yes         | `var age = 25;`         |
| `final` | ❌ No          | `final name = 'Alice';` |

### Quick memory trick

```text
var   → value can change
final → value is assigned once
```

---

# 8. Common Variable Examples

```dart
int number = 5;

var age = 25;

final name = 'Alice';
```

---

# 9. Quick Summary

### String length

```dart
'hello'.length
```

### Explicit variable type

```dart
int number = 5;
```

### Declaration + assignment

```dart
int number;
number = 6;
```

### `var`

```dart
var age = 25;
age = 30;
```

### `final`

```dart
final name = 'Alice';
```

### Important

```text
var   → can be reassigned
final → cannot be reassigned
```

---

## Remember

**Dart supports type inference**, so you often don't need to explicitly write the variable's type.

```dart
int age = 25;   // Explicit type

var age = 25;   // Type inferred as int
```




# Dart: Numbers

| Type     | Use              | Example      |
| -------- | ---------------- | ------------ |
| `int`    | Whole numbers    | `25`         |
| `double` | Decimal numbers  | `3.14`       |
| `num`    | `int` + `double` | `25`, `3.14` |

## `int`

```dart
int age = 25;
int hex = 0xFF; // 255
```

No decimals:

```dart
int x = 3.14; // Error
```

## `double`

```dart
double price = 3.14;
double x = 1.5e5; // 150000.0
```

## Automatic Conversion

```dart
double x = 1;
print(x); // 1.0
```

## Remember

```text
int    → whole
double → decimal
num    → both
0x     → hexadecimal
e5     → × 10⁵
```

**Best practice:** Use `int` or `double` when possible; use `num` when both are needed.





# Dart: Strings

## String

A `String` is a sequence of characters/text.

```dart
String name = 'Dart';
```

Strings can use single or double quotes:

```dart
'Hello'
"Hello"
```

## Escape Characters

Use `\` to escape special characters.

```dart
'It\'s Dart'
"It's Dart"

print('\$5'); // $5
```

## Concatenation

Use `+` to join strings.

```dart
String first = 'Hello';
String second = 'World';

print(first + ' ' + second);
```

Output:

```text
Hello World
```

## String Interpolation

Insert variables using `$`.

```dart
String name = 'Alice';

print('Hello $name');
```

For expressions, use `${}`:

```dart
print('Result: ${5 + 3}');
```

Output:

```text
Result: 8
```

## Length & Indexing

`.length` → number of characters.

```dart
String greeting = 'Hello';

print(greeting.length); // 5
print(greeting[0]);     // H
```

Dart uses **zero-based indexing**:

```text
H  e  l  l  o
0  1  2  3  4
```

Last character:

```dart
print(greeting[greeting.length - 1]);
```

> Dart does **not** support negative indexing.

## Useful Methods

```dart
String text = 'Dart Programming';

print(text.toUpperCase()); // DART PROGRAMMING
print(text.toLowerCase()); // dart programming
print(text.substring(0, 4)); // Dart
```

### Strings are Immutable

Strings cannot be changed after they are created.

String methods return a **new string**.

```dart
String text = 'Dart';

String upper = text.toUpperCase();

print(text);  // Dart
print(upper); // DART
```

## Multiline Strings

Use triple quotes:

```dart
String message = '''
Hello
World
Dart
''';
```

### Adjacent Literals

Adjacent strings are automatically joined:

```dart
String text = 'Hello '
              'World';
```

Output:

```text
Hello World
```

## Quick Reference

```text
String       → text
+            → concatenate
$variable    → interpolation
${expression}→ expression interpolation
\$           → literal $
.length      → string length
[index]      → access character
.length - 1  → last character
.toUpperCase() → uppercase
.toLowerCase() → lowercase
.substring() → extract part
''' '''      → multiline string
```

> **Remember:** Dart strings are **immutable** and use **zero-based indexing**.



```dart

```