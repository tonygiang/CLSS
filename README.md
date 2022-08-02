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

If you ever felt like these irregularities should not have existed to provide better consistency, CLSS suite offers a solution for you. It fills in the gaps left by the Standard Library. Its XML comments do the best to resemble ones that ship with classes and methods in the SL. Its implementations try to follow the [.NET reference source](https://referencesource.microsoft.com/) as closely as possible. CLSS suite is built to make the SL feel **complete**.

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

- [CLSS.Constants.DefaultRandom](https://www.nuget.org/packages/CLSS.Constants.DefaultRandom) ([Source](https://github.com/tonygiang/CLSS.Constants.DefaultRandom))

- [CLSS.Constants.NoOp](https://www.nuget.org/packages/CLSS.Constants.NoOp) ([Source](https://github.com/tonygiang/CLSS.Constants.NoOp))

- [CLSS.ExtensionMethods.CommonMathOps](https://www.nuget.org/packages/CLSS.ExtensionMethods.CommonMathOps) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.CommonMathOps))

- [CLSS.ExtensionMethods.IComparable.InRange](https://www.nuget.org/packages/CLSS.ExtensionMethods.IComparable.InRange) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IComparable.InRange))

- [CLSS.ExtensionMethods.IDictionary.GetOrAdd](https://www.nuget.org/packages/CLSS.ExtensionMethods.IDictionary.GetOrAdd) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IDictionary.GetOrAdd))

- [CLSS.ExtensionMethods.IDictionary.MoveKey](https://www.nuget.org/packages/CLSS.ExtensionMethods.IDictionary.MoveKey) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IDictionary.MoveKey))

- [CLSS.ExtensionMethods.IEnumerable.ForEach](https://www.nuget.org/packages/CLSS.ExtensionMethods.IEnumerable.ForEach) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IEnumerable.ForEach))

- [CLSS.ExtensionMethods.IEnumerable.MinMaxBy](https://www.nuget.org/packages/CLSS.ExtensionMethods.IEnumerable.MinMaxBy) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IEnumerable.MinMaxBy))

- [CLSS.ExtensionMethods.IList.FillBy](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.FillBy) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.FillBy))

- [CLSS.ExtensionMethods.IList.FirstLastIndex](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.FirstLastIndex) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.FirstLastIndex))

- [CLSS.ExtensionMethods.IList.SwapIndices](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.SwapIndices) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.IList.SwapIndices))

- [CLSS.ExtensionMethods.Object.As](https://www.nuget.org/packages/CLSS.ExtensionMethods.Object.As) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.Object.As))

- [CLSS.ExtensionMethods.Object.Is](https://www.nuget.org/packages/CLSS.ExtensionMethods.Object.Is) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.Object.Is))

- [CLSS.ExtensionMethods.Pipe](https://www.nuget.org/packages/CLSS.ExtensionMethods.Pipe) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.Pipe))

- [CLSS.ExtensionMethods.String.AsEnum](https://www.nuget.org/packages/CLSS.ExtensionMethods.String.AsEnum) ([Source](https://github.com/tonygiang/CLSS.ExtensionMethods.String.AsEnum))

- [CLSS.Types.MemoizedFunc](https://www.nuget.org/packages/CLSS.Types.MemoizedFunc) ([Source](https://github.com/tonygiang/CLSS.Types.MemoizedFunc))

- [CLSS.Types.Reference](https://www.nuget.org/packages/CLSS.Types.Reference) ([Source](https://github.com/tonygiang/CLSS.Types.Reference))

- [CLSS.Types.SortedAction](https://www.nuget.org/packages/CLSS.Types.SortedAction) ([Source](https://github.com/tonygiang/CLSS.Types.SortedAction))

- [CLSS.Types.ValueRange](https://www.nuget.org/packages/CLSS.Types.ValueRange) ([Source](https://github.com/tonygiang/CLSS.Types.ValueRange))