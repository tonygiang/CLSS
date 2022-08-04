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
