## 2024-05-18 - Dictionary ContainsKey Optimization
**Learning:** In C# Dictionary, using `TryGetValue` instead of checking `ContainsKey` and then indexing into the dictionary is more efficient because it avoids a double lookup.
**Action:** Replace `if (dict.ContainsKey(key)) { value = dict[key]; ... }` with `if (dict.TryGetValue(key, out var value)) { ... }` where applicable.
