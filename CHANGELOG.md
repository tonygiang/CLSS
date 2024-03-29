# Update 9 - 2024-02-16

### Version updates

- `CLSS.Constants.CollectionPool` 1.0.0 > 1.1.0
  - Updated package dependency.
- `CLSS.ExtensionMethods.IComparable.ClampToRange` 1.2.0 > 1.3.0
  - Renamed the version for non-generic IComparable for better compatibility with types that implement both generic and non-generic IComparable.
- `CLSS.ExtensionMethods.IDictionary.SwapKeys` 1.1.1 > 1.1.2
  - Fixed minor errors in README file.
- `CLSS.ExtensionMethods.IEnumerable.MinMaxBy` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IEnumerator.LoopNext` 1.0.1 > 1.0.2
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IList.FillBy` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IList.FirstLastIndex` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
  - Fixed a minor error in README file.
- `CLSS.ExtensionMethods.IList.GetLoopingElementAt` 1.0.0 > 1.0.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IList.GetRandom` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IList.GetWeightedRandom` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IList.Shuffle` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IList.SwapIndices` 1.2.0 > 1.2.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.Object.As` 1.0.0 > 1.0.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.Object.Is` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.Object.ToStringFormattedBy` 1.0.0 > 1.0.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.Reference.Action.Once` 1.0.0 > 1.0.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.Types.AgnosticObjectPool` 1.0.1 > 1.1.0
  - Fixed an IndexOutOfRangeException when TakeOne triggers a growth.
- `CLSS.Types.EventLatch` 1.0.0 > 1.0.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.Types.Reference` 1.0.0 > 1.0.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.Types.SortedAction` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.Types.ValueRange` 1.0.1 > 1.1.0
  - Added Encapsulate extension method.

# Update 8 - 2022-11-16

### Version updates

- `CLSS.Constants.DefaultRandom` 1.2.0 > 1.2.1
  - Improved comment.
- `CLSS.Constants.NoOp` 1.0.0 > 1.0.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.Constants.ValueEquivalentStrings` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.CommonMathOps` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IComparable.ClampToRange` 1.1.0 > 1.2.0
  - Added language-sensitive syntax highlighting in README file.
  - Added Unity-specific compilation directive.
- `CLSS.ExtensionMethods.IComparable.InRange` 1.2.0 > 1.3.0
  - Added language-sensitive syntax highlighting in README file.
  - Added Unity-specific compilation directive.
- `CLSS.ExtensionMethods.IDictionary.GetOrAdd` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IDictionary.MoveKey` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IDictionary.RemoveAndProcess` 1.0.0 > 1.0.1
  - Changed XML comment to better reflect the order of execution.
- `CLSS.ExtensionMethods.IDictionary.SwapKeys` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IEnumerable.ForEach` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IEnumerable.Looping` 1.1.0 > 1.1.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.IList.RemoveAndProcess` 1.0.0 > 1.0.1
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.ExtensionMethods.String.AsEnum` 1.0.0 > 1.0.1
  - Fixed grammatical error in README.
  - Added language-sensitive syntax highlighting in README file.
- `CLSS.Types.AgnosticObjectPool` 1.0.0 > 1.0.1
  - Improved comment.
  - Improved README description.
- `CLSS.Types.ValueRange` 1.0.0 > 1.0.1
  - Improved comment.
  - Added language-sensitive syntax highlighting in README file.
  
### New packages

- [`CLSS.Constants.CollectionPool`](https://www.nuget.org/packages/CLSS.Constants.CollectionPool): A collection of statically-defined pools of Base Class Library's built-in collection types.

# Update 7 - 2022-10-05

This is a hotfix update.

### Version updates

- `CLSS.Types.MemoizedFunc` 1.1.0 > 1.2.0
  - Remove the dependency on System.ValueTuple on .NET Standard 2.0.
  - Add language-sensitive syntax highlighting in README file.

# Update 6 - 2022-08-31

### Version updates

- `CLSS.ExtensionMethods.Pipe` 1.2.0 > 1.3.0
  - Reversed support for BCL delegate types since they create ambiguous issue.
  - Improved comment for type parameters.
  - Experimental support for language-sensitive syntax highlighting in README file.
- Deprecated version 1.2.0 of `CLSS.ExtensionMethods.Pipe` due to the method ambiguity issue created by the addition of overloads for built-in BCL delegate types.

### New packages

- [`CLSS.ExtensionMethods.IDictionary.RemoveAndProcess`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IDictionary.RemoveAndProcess): An extension method that combines the removal of a key from an IDictionary and post-removal processing of that key's associated value into one method call.
- [`CLSS.ExtensionMethods.IList.RemoveAndProcess`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.RemoveAndProcess): An extension method that combines the removal of an element from an IList and post-removal processing of that element into one method call.
- [`CLSS.Types.AgnosticObjectPool`](https://www.nuget.org/packages/CLSS.Types.AgnosticObjectPool): A domain-agnostic object pool that only handles pooling logic and lets you customize object creation and availability checking logic.

# Update 5 - 2022-08-20

### New packages

- [`CLSS.ExtensionMethods.Reference.Action.Once`](https://www.nuget.org/packages/CLSS.ExtensionMethods.Reference.Action.Once): An extension method to register a listener to a delegate that will only execute once.
- [`CLSS.Types.EventLatch`](https://www.nuget.org/packages/CLSS.Types.EventLatch): A synchronisation aid object for single-threaded context.

# Update 4 - 2022-08-13

This is a maintenance update mainly to make CLSS packages depending on other CLSS packages to always use the latest version of the dependency.

### Version updates

- `CLSS.Constants.ValueEquivalentStrings` 1.0.0 > 1.1.0
  - Automatically use the latest CLSS dependency version.
- `CLSS.ExtensionMethods.IComparable.ClampToRange` 1.0.0 > 1.1.0
  - Automatically use the latest CLSS dependency version.
- `CLSS.ExtensionMethods.IComparable.InRange` 1.1.0 > 1.2.0
  - Automatically use the latest CLSS dependency version.
- `CLSS.ExtensionMethods.IDictionary.SwapKeys` 1.0.0 > 1.1.0
  - Removed unnecessary dependency on CLSS.Types.ValueRange.
- `CLSS.ExtensionMethods.IEnumerable.Looping` 1.0.0 > 1.1.0
  - Automatically use the latest CLSS dependency version.
- `CLSS.ExtensionMethods.IList.ExclusiveSample` 1.0.0 > 1.1.0
  - Automatically use the latest CLSS dependency version.
- `CLSS.ExtensionMethods.IList.GetWeightedRandom` 1.0.0 > 1.1.0
  - Automatically use the latest CLSS dependency version.
- `CLSS.ExtensionMethods.IList.Shuffle` 1.0.0 > 1.1.0
  - Automatically use the latest CLSS dependency version.
- `CLSS.Types.WeightedSampler` 1.0.0 > 1.1.0
  - Automatically use the latest CLSS dependency version.

# Update 3 - 2022-08-11

### Version updates

- `CLSS.ExtensionMethods.IComparable.InRange` 1.1.0 > 1.1.1
  - Corrected a spelling error in README.
- `CLSS.ExtensionMethods.Pipe` 1.1.0 > 1.2.0
  - Added support for Converter (.NET Standard 2.0 only) and Predicate delegates from BCL.

### New packages

- [`CLSS.Constants.ValueEquivalentStrings`](https://www.nuget.org/packages/CLSS.Constants.ValueEquivalentStrings): A global cache of default string representations of values of value types.
- [`CLSS.ExtensionMethods.IEnumerable.Looping`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IEnumerable.Looping): An extension method create an enumerable that infinitely loops over a collection.
- [`CLSS.ExtensionMethods.IList.GetLoopingElementAt`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.GetLoopingElementAt): An extension method to cyclically convert any integer number into a valid index to get an element from a list.

# Update 2 - 2022-08-07

### Version updates

- `CLSS.Constants.DefaultRandom` 1.1.0 > 1.2.0
  - Improve the thread safetyness of DefaultRandom by making it atomic.
- `CLSS.ExtensionMethods.IComparable.InRange` 1.0.0 > 1.1.0
  - Add an overload taking in ValueRange for .NET Standard 2.0.
- `CLSS.ExtensionMethods.IList.SwapIndices` 1.1.0 > 1.2.0
  - Update README to correct grammar errors.

### New packages

- [`CLSS.ExtensionMethods.IComparable.ClampToRange`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IComparable.ClampToRange): An extension method to clamp the source value into a range.
- [`CLSS.ExtensionMethods.IDictionary.SwapKeys`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IDictionary.SwapKeys): An extension method to swap the values at 2 different keys in an IDictionary.
- [`CLSS.ExtensionMethods.IEnumerator.LoopNext`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IEnumerator.LoopNext): An extension method to infinitely advance an enumerator in a loop.
- [`CLSS.ExtensionMethods.Object.ToStringFormattedBy`](https://www.nuget.org/packages/CLSS.ExtensionMethods.Object.ToStringFormattedBy): An extension method to transform one or several objects into string form following a particular format.

# Update 1 - 2022-08-04

### Version updates

- `CLSS.Constants.DefaultRandom` 1.0.0 > 1.1.0
  - Made the Random instance thread-safe.
- `CLSS.ExtensionMethods.CommonMathOps` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.ExtensionMethods.IDictionary.GetOrAdd` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.ExtensionMethods.IDictionary.MoveKey` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.ExtensionMethods.IEnumerable.ForEach` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.ExtensionMethods.IEnumerable.MinMaxBy` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
  - Correct an error in empty collection detection that causes collections with 1 or more elements to throw InvalidOperationException.
- `CLSS.ExtensionMethods.IList.FillBy` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.ExtensionMethods.IList.FirstLastIndex` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.ExtensionMethods.IList.SwapIndices` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.ExtensionMethods.Object.Is` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.ExtensionMethods.Pipe` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.Types.MemoizedFunc` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- `CLSS.Types.SortedAction` 1.0.0 > 1.1.0
  - Reduce comment redundancy.
- Deprecated version 1.0.0 of `CLSS.ExtensionMethods.IEnumerable.MinMaxBy` due to the empty collection detection error.

### New packages

- [`CLSS.ExtensionMethods.IList.ExclusiveSample`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.ExclusiveSample): An extension method to randomly selection a number of non-repeating elements out of an IList using Donald Knuth's Algorithm S (Selection sampling technique).
- [`CLSS.ExtensionMethods.IList.GetRandom`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.GetRandom): An extension method to select a random element from a list.
- [`CLSS.ExtensionMethods.IList.GetWeightedRandom`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.GetWeightedRandom): An extension method to select a weighted random element from a list.
- [`CLSS.ExtensionMethods.IList.Shuffle`](https://www.nuget.org/packages/CLSS.ExtensionMethods.IList.Shuffle): An extension method to shuffle an IList in place using the Fisher-Yates algorithm.
- [`CLSS.Types.WeightedSampler`](https://www.nuget.org/packages/CLSS.Types.WeightedSampler): A struct type that wraps around a list collection to select a weighted random element from it efficiently.
