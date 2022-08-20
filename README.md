# CLSS - The C# Language Syntactic Sugar suite

A collection of independent or loosely-coupled packages to enhance the syntax of C# in a minimal way.

## Why CLSS?

The C# Language Syntactic Sugar suite was created out of my frustration working with C#. The language and its Class Library have not evolved fast enough to address the inconsistencies, performance traps, unintuitiveness and lacking accommodation of common use-cases despite it is very much inline with the language's tradition to accommodate such use-cases. Did you know that the Class Library ships with a [Version](https://docs.microsoft.com/en-us/dotnet/api/system.version?view=net-6.0) type that parses version strings in the `major.minor[.build[.revision]]` syntax and also programmatically implements `IComparable<T>` and `IEquatable<T>`?

Even when these concerns are addressed, they only come to the latest versions of the language and Class Library. Working in a bleeding-edge .NET environment is a luxury for many developers.

Our good friends such as [language-ext](https://github.com/louthy/language-ext), [csharp-extensions](https://github.com/rmandvikar/csharp-extensions) and [CSharpFunctionalExtensions](https://github.com/vkhorikov/CSharpFunctionalExtensions) made great efforts to address such concerns but one issue remains. Like many other language extension packages, their monolithic structure creates a high risk of conflicting with existing extension methods in your own projects once you `using` their namespaces.

CLSS set out to go in a different direction.

## Modular

CLSS suite embraces the [Unix philosophy](https://en.wikipedia.org/wiki/Unix_philosophy).  CLSS tried not to be one monolothic package but rather an umbrella for multiple packages. Each package is laser-focused on providing one functionality and can be installed (mostly) independently of other packages. Only install what you want and what is compatible with your current project, and no more.

## Natural

There are several irregulaties in the .NET Standard Library.

Why is there a [`GetOrAdd`](https://docs.microsoft.com/en-us/dotnet/api/system.collections.concurrent.concurrentdictionary-2.getoradd?view=net-6.0) method for `ConcurrentDictionary` but not for other Dictionary types?

Why is there a [`ForEach`](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1.foreach?view=net-6.0) method for `List<T>` but not for other iteratable collections?

Why does [`Enum.Parse`](https://docs.microsoft.com/en-us/dotnet/api/system.enum.parse?view=net-6.0) allow non-Enum value types in its type parameter?

If you ever felt like these irregularities should not have existed to provide better consistency, CLSS suite offers a solution for you. It fills in the gaps left by the Base Class Library. Its XML comments do the best to resemble ones that ship with classes and methods in the BCL. Its implementations try to follow the [.NET reference source](https://referencesource.microsoft.com/) as closely as possible. CLSS suite is built to make the BCL feel **complete**.

Inkeeping with the intent to feel like a natural part of the language and its Class Library, CLSS will be averse to being revolutionary such as language-ext. CLSS packages may lean toward the syntax of functional programming, but will commit to the familiarity of the C# syntax. No monad or endofunctor here. Just functional programming the way you can still recognize as C#.

## Polyfilling

A secondary goal of CLSS suite is to polyfill for older language versions and .NET versions. Some of the features from new .NET versions that CLSS can polyfill are: LINQ `MaxBy`/`MinBy`, shared `Random` instance and array filling.

CLSS packages multi-target .NET Standard 2.0 and - wherever possible - as low as .NET Standard 1.0. Learn how compatible these standards are [here](https://dotnet.microsoft.com/en-us/platform/dotnet-standard).

## How to install & use

You can find and install every CLSS packages under the ['CLSS' tag on the NuGet Gallery](https://www.nuget.org/packages?q=Tags%3A%22CLSS%22).

To start using CLSS packages after installing, add this line to the top of your C# source file:

```
using CLSS;
```

## How to contribute

Package-specific issues should be submitted to their respective repositories. If you have an idea that you think should make it into the shared `CLSS` namespace, submit an issue to this repository.

## What this suite contains

Below is the list of packages contained in the CLSS suite so far:

- [`CLSS.Constants.DefaultRandom`](https://www.nuget.org/packages/CLSS.Constants.DefaultRandom) ([Source](https://github.com/tonygiang/CLSS.Constants.DefaultRandom)): A default-constructed instance of the System.Random class.
- [`CLSS.Constants.NoOp`](https://www.nuget.org/packages/CLSS.Constants.NoOp) ([Source](https://github.com/tonygiang/CLSS.Constants.NoOp)): A collection of statically-defined No-op methods used in place of anonymous no-ops to save memory allocations.
- [`CLSS.ExtensionMethods.CommonMathOps`](https://www.nuget.org/packages/CLSS.ExtensionMethods.CommonMathOps) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.CommonMathOps)): A collection of common math operations in a functional syntax.
- [`CLSS.ExtensionMethods.IComparable.InRange`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IComparable.InRange) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IComparable.InRange)): An extension method to check whether the source value is within a range.
- [`CLSS.ExtensionMethods.IDictionary.GetOrAdd`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IDictionary.GetOrAdd) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IDictionary.GetOrAdd)): An extension method to provide GetOrAdd as found in ConcurrentDictionary to every IDictionary type.
- [`CLSS.ExtensionMethods.IDictionary.MoveKey`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IDictionary.MoveKey) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IDictionary.MoveKey)): An extension method to move the value of a dictionary's key to another key.
- [`CLSS.ExtensionMethods.IEnumerable.ForEach`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IEnumerable.ForEach) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IEnumerable.ForEach)): An extension method to provide ForEach as found in List to every IEnumerable type.
- [`CLSS.ExtensionMethods.IEnumerable.MinMaxBy`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IEnumerable.MinMaxBy) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IEnumerable.MinMaxBy)): An extension method to provide MinBy and MaxBy as found in .NET 6 to projects running on an earlier runtime version.
- [`CLSS.ExtensionMethods.IList.FillBy`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.FillBy) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.FillBy)): An extension method to fill all indices of an IList with a default value.
- [`CLSS.ExtensionMethods.IList.FirstLastIndex`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.FirstLastIndex) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.FirstLastIndex)): An extension method to find the first or last index of an IList element matching a condition.
- [`CLSS.ExtensionMethods.IList.SwapIndices`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.SwapIndices) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.SwapIndices)): An extension method to swap the values at 2 different indices in an IList.
- [`CLSS.ExtensionMethods.Object.As`](https://www.nuget.org/packages/CLSS.ExtensionMethods.Object.As) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.Object.As)): An extension method to cast reference types in a functional-style syntax.
- [`CLSS.ExtensionMethods.Object.Is`](https://www.nuget.org/packages/CLSS.ExtensionMethods.Object.Is) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.Object.Is)): An extension method to check reference types in a functional-style syntax.
- [`CLSS.ExtensionMethods.Pipe`](https://www.nuget.org/packages/CLSS.ExtensionMethods.Pipe) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.Pipe)): An extension method to replicate the pipe syntax (take the source value and feed it as an argument to a method).
- [`CLSS.ExtensionMethods.String.AsEnum`](https://www.nuget.org/packages/CLSS.ExtensionMethods.String.AsEnum) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.String.AsEnum)): An extension method to provide a type-safe and functional style way to convert strings to enums.
- [`CLSS.Types.MemoizedFunc`](https://www.nuget.org/packages/CLSS.Types.MemoizedFunc) ([Source](https://github.com/tonygiang/CLSS.Types.MemoizedFunc)): A class that encapsulates a function to automatically memoize its results.
- [`CLSS.Types.Reference`](https://www.nuget.org/packages/CLSS.Types.Reference) ([Source](https://github.com/tonygiang/CLSS.Types.Reference)): A class that encapsulates a single value with the primary intention of making value types referenceable.
- [`CLSS.Types.SortedAction`](https://www.nuget.org/packages/CLSS.Types.SortedAction) ([Source](https://github.com/tonygiang/CLSS.Types.SortedAction)): A delegate-like type that allows executions by key order.
- [`CLSS.Types.ValueRange`](https://www.nuget.org/packages/CLSS.Types.ValueRange) ([Source](https://github.com/tonygiang/CLSS.Types.ValueRange)): A type-safe, serializable generic struct type tailored to semantically represent a range of comparable values.

##### New in Update 1:

- [`CLSS.ExtensionMethods.IList.ExclusiveSample`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.ExclusiveSample) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.ExclusiveSample)): An extension method to randomly selection a number of non-repeating elements out of an IList using Donald Knuth's Algorithm S (Selection sampling technique).
- [`CLSS.ExtensionMethods.IList.GetRandom`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.GetRandom) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.GetRandom)): An extension method to select a random element from a list.
- [`CLSS.ExtensionMethods.IList.GetWeightedRandom`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.GetWeightedRandom) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.GetWeightedRandom)): An extension method to select a weighted random element from a list.
- [`CLSS.ExtensionMethods.IList.Shuffle`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.Shuffle) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.Shuffle)): An extension method to shuffle an IList in place using the Fisher-Yates algorithm.
- [`CLSS.Types.WeightedSampler`](https://www.nuget.org/packages/CLSS.Types.WeightedSampler) ([Source](https://github.com/tonygiang/CLSS.Types.WeightedSampler)): A struct type that wraps around a list collection to select a weighted random element from it efficiently.

##### New in Update 2:

- [`CLSS.ExtensionMethods.IComparable.ClampToRange`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IComparable.ClampToRange) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IComparable.ClampToRange)): An extension method to clamp the source value into a range.
- [`CLSS.ExtensionMethods.IDictionary.SwapKeys`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IDictionary.SwapKeys) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IDictionary.SwapKeys)): An extension method to swap the values at 2 different keys in an IDictionary.
- [`CLSS.ExtensionMethods.IEnumerator.LoopNext`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IEnumerator.LoopNext) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IEnumerator.LoopNext)): An extension method to infinitely advance an enumerator in a loop.
- [`CLSS.ExtensionMethods.Object.ToStringFormattedBy`](https://www.nuget.org/packages/CLSS.ExtensionMethods.Object.ToStringFormattedBy) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.Object.ToStringFormattedBy)): An extension method to transform one or several objects into string form following a particular format.

##### New in Update 3:

- [`CLSS.Constants.ValueEquivalentStrings`](https://www.nuget.org/packages/CLSS.Constants.ValueEquivalentStrings) ([Source](https://github.com/tonygiang/CLSS.Constants.ValueEquivalentStrings)): A global cache of default string representations of values of value types.
- [`CLSS.ExtensionMethods.IEnumerable.Looping`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IEnumerable.Looping) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IEnumerable.Looping)): An extension method create an enumerable that infinitely loops over a collection.
- [`CLSS.ExtensionMethods.IList.GetLoopingElementAt`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.GetLoopingElementAt) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.GetLoopingElementAt)): An extension method to cyclically convert any integer number into a valid index to get an element from a list.

##### New in Update 5:

- [`CLSS.ExtensionMethods.Reference.Action.Once`](https://www.nuget.org/packages/CLSS.ExtensionMethods.Reference.Action.Once) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.Reference.Action.Once)): An extension method to register a listener to a delegate that will only execute once.
- [`CLSS.Types.EventLatch`](https://www.nuget.org/packages/CLSS.Types.EventLatch) ([Source](https://github.com/tonygiang/CLSS.Types.EventLatch)): A synchronisation aid object for single-threaded context.