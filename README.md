Download Link: https://assignmentchef.com/product/solved-ocaml-discussion-3-introduction-to-ocaml
<br>
This exercise consists of a few short functions to help you familiarize yourself with OCaml. You can review the content of the discussion in [notes.rb](notes.rb), which includes the topics and examples from the discussion video. Also, check out [utop-tutorial.md](utop-tutorial.md) for an introduction to using `utop`.

## Part 1: Type inference

At the top of [disc3.ml](src/disc3.ml), there are a few function definitions. Try determining the types of these functions and check your answers with `utop`. This portion of the discussion is not tested (and thus not graded), but these kinds of exercises may appear on quizzes and exams!

## Part 2: Type definitions

You will have to fill in definitions for the functions `tf1`, `tf2`, `tf3` such that they have the type that is expected in the `.mli`. The operation of the function does not matter, as long as they have the correct types.

#### `tf1 a`

– **Type**: `string -&gt; int`

#### `tf2 a b c`

– **Type**: `’a -&gt; ‘b -&gt; ‘b -&gt; bool`

#### `tf3 a b`

– **Type**: `’a list -&gt; ‘a list -&gt; ‘a`– **Note**: For this one, you can assume that the lists `a` and `b` are not empty.

## Part 3: Functions

#### `concat str1 str2`

– **Type**: `string -&gt; string -&gt; string`– **Description**: Appends `str2` to the end of `str1`.– **Examples**:“`ocamlconcat “” “” = “”concat “” “abc” = “abc”concat “xyz” “” = “xyz”concat “abc” “xyz” = “abcxyz”“`

#### `add_to_float integer flt`

– **Type**: `int -&gt; float -&gt; float`– **Description**: Adds `integer` and `flt` and returns a float representation of the sum.– **Examples**:“`ocamladd_to_float 3 4.8 = 7.8add_to_float 0 0.0 = 0.0“`

#### `fib n`

– **Type**: `int -&gt; int`– **Description**: Calculates the nth [Fibonacci number](https://en.wikipedia.org/wiki/Fibonacci_number).– **Examples**:“`ocamlfib 0 = 0fib 1 = 1fib 2 = 1fib 3 = 2fib 6 = 8“`

## Part 4: Lists

#### `add_three lst`

– **Type**: `int list -&gt; int list`– **Description**: Adds 3 to each element in `lst`.– **Examples**:“`ocamladd_three [] = []add_three [1] = [4]add_three [1; 3; 5] = [4; 6; 8]“`

#### `filter n lst`

– **Type**: `int -&gt; int list -&gt; int list`– **Description**: Given an integer `n` and a list `lst`, Remove elements from `lst` that are greater than `n`.– **Examples**:“`ocamlfilter 2 [1; 2; 3; 3; 2; 1] = [1; 2; 2; 1]filter 5 [-1; 2; 3; 4] = [-1; 2; 3; 4]“`

#### `double lst`

– **Type**: `’a list -&gt; ‘a list`– **Description**: Given a list `lst`, return a new list that has two copies of every element in `lst`.– **Examples**:“`ocamldouble [1;2;3;4] = [1;1;2;2;3;3;4;4]double [“a”; “b”; “c”] = [“a”; “a”; “b”; “b”; “c”; “c”]“`