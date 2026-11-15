**Date:** 27/10/2026

### Problem

The Futures For All scraper crashed when trying to parse the API response as JSON.

Error message:
```text
System.Text.Json.JsonReaderException:
'S' is an invalid start of a value.
```

### Cause

The `GettingJson()` method was called without `await`, so the asynchronous operation wasn't being handled correctly before the JSON parsing step.

### Solution

Added `await` when calling the method:

```csharp
string json = await GettingJson();
```

This ensures the JSON retrieval completes before the response is passed to the parser.

**Status:** Fixed.
