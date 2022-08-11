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
