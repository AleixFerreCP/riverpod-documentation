`Freezed` is a library in Flutter that simplifies the creation of immutable classes and data patterns. It is particularly useful for defining data models that need 
serialization, deep comparisons, and safe copying.

`Freezed` is a code generation library that works with the `build_runner` package to create immutable classes. It leverages Dart's annotation system to automatically generate boilerplate code, which includes:

- Equality operators (`==` and `hashCode`)
- CopyWith methods
- JSON serialization and deserialization
- Union types and sealed classes
- Deep comparisons
