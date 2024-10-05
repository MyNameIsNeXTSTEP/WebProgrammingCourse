[The wikipedia says](https://en.wikipedia.org/wiki/Data_type)

> In [computer science](https://en.wikipedia.org/wiki/Computer_science "Computer science") and [computer programming](https://en.wikipedia.org/wiki/Computer_programming "Computer programming"), a **data type** (or simply **type**) is a collection or grouping of data values, usually specified by a set of possible values, a set of allowed operations on these values, and/or a representation of these values as machine types.
> A data type specification in a program constrains the possible values that an [expression](https://en.wikipedia.org/wiki/Expression_(computer_science) "Expression (computer science)"), such as a variable or a function call, might take. On literal data, it tells the [compiler](https://en.wikipedia.org/wiki/Compiler "Compiler") or [interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing) "Interpreter (computing)") how the programmer intends to use the data. Most programming languages support basic data types of [integer](https://en.wikipedia.org/wiki/Integer_(computer_science) "Integer (computer science)") numbers (of varying sizes), [floating-point](https://en.wikipedia.org/wiki/Floating_point "Floating point") numbers (which approximate [real numbers](https://en.wikipedia.org/wiki/Real_number "Real number")), [characters](https://en.wikipedia.org/wiki/Character_(computing) "Character (computing)") and [Booleans](https://en.wikipedia.org/wiki/Boolean_data_type "Boolean data type").

## Definition

We can define data types as following behavioral or/and semantical descriptions. ([Link](https://en.wikipedia.org/wiki/Data_type#CITEREFParnasShoreWeiss1976))

"A type is":

1. **Syntactic label** associated with a variable (in case of programming - the programm unit) when it is declared.
2. Defined as a **representation** in terms of a composition of more primitive types — often machine types.
3. Defined as program unit **behavioral** descriptive with a set of operators manipulating on these representations.
4. Set of possible **values** which a variable can possess.
5. Set of **values** which a variable can possess and a set of functions that one can apply to these values.

---

## Examples

**<u>Non-composite types</u>

#### Machine data types
All data in computers based on digital electronics is represented as [bits](https://en.wikipedia.org/wiki/Bit "Bit") (alternatives 0 and 1) on the lowest level. The smallest addressable unit of data is usually a group of bits called a [byte](https://en.wikipedia.org/wiki/Byte "Byte") (usually an [octet](https://en.wikipedia.org/wiki/Octet_(computing) "Octet (computing)"), which is 8 bits). The unit processed by [machine code](https://en.wikipedia.org/wiki/Machine_code "Machine code") instructions is called a [word](https://en.wikipedia.org/wiki/Word_(data_type) "Word (data type)") typically 32 or 64 bits).

**Machine data** types _expose_ or make available fine-grained control over hardware, but this can also expose implementation details that make code less portable. Hence machine types are mainly used in [systems programming](https://en.wikipedia.org/wiki/Systems_programming "Systems programming") or [low-level programming languages](https://en.wikipedia.org/wiki/Low-level_programming_language "Low-level programming language"). In higher-level languages most data types are _abstracted_ in that they do not have a language-defined machine representation. The [C programming language](https://en.wikipedia.org/wiki/C_programming_language "C programming language"), for instance, supplies types such as Booleans, integers, floating-point numbers, etc., but the precise bit representations of these types are implementation-defined.

#### Boolean
The **boolean** type represents the discrete values of true and false.
Many programming languages do not have an explicit Boolean type, instead using an integer type and interpreting (for instance) 0 as false and other values as true. Boolean data refers to the logical structure of how the language is interpreted to the machine language. In this case a Boolean 0 refers to the logic False. True is always a non zero, especially a one which is known as Boolean 1.

#### Numeric
First of all we need to say that numerics in machines in common usage are collection of discrete or continuous values that convey information, describing the *quantity*, *amount*, *statistics*, other basic units of humanazed meaning of a **number**, or simply sequences of symbols that may be further interpreted formally as numbers.

From the very beginning since there are unit of information in computers we knoiw as bits and bytes, the numeric type has become, first of all in low-level programming languages, classified into a group of numeric types such as:
- Integer (signed, unsigned, short, long, double)
- Float (floating points)

#### Strings and text
Strings are a sequence of characters used to store words or plain text.
Characters may be a letter of somealphabet, a digit, a blank space, a punctuation mark, etc. Characters are drawn from a character set such as [ASCII](https://en.wikipedia.org/wiki/ASCII "ASCII"). Character and string types can have different subtypes according to the character encoding. The original 7-bit wide ASCII was found to be limited, and superseded by 8, 16 and 32-bit sets, which can encode a wide variety of non-Latin alphabets, and other symbols. Strings may be of either variable length or fixed length, and some programming languages have both types. They may also be subtyped by their maximum size.

Since most character sets include the [digits](https://en.wikipedia.org/wiki/Numerical_digit "Numerical digit"), it is possible to have a numeric string, such as `"1234"`. These numeric strings are usually considered distinct from **numeric values** such as `1234`, although some languages automatically convert between them.

---

**<u>Composite types</u>

Enumerations
Union types
Abstract data types
Pointers and referrences
Function type
Quantified types
Meta types
Convinience types

[More here](https://en.wikipedia.org/wiki/Data_type)