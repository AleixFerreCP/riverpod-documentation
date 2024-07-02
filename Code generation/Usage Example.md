1. **Add dependencies** in your `pubspec.yaml`:

```yaml
    dependencies:
      freezed_annotation: ^2.0.0

    dev_dependencies:
      build_runner: ^2.1.0
      freezed: ^2.0.0
      json_serializable: ^6.0.0
```

2. **Create a data class** using `Freezed`:

```dart
    import 'package:freezed_annotation/freezed_annotation.dart';

    part 'user.freezed.dart';
    part 'user.g.dart';

    @freezed
    class User with _$User {
      const factory User({
        required String id,
        required String name,
        required int age,
      }) = _User;

      factory User.fromJson(Map<String, dynamic> json) => _$UserFromJson(json);
    }
```

3. **Run the code generator**:

```bash
    flutter pub run build_runner build
```

4. **Use the generated code**:

```dart
void main() {
  final user = User(id: '123', name: 'Alice', age: 30);

  // Copying with a new age
  final updatedUser = user.copyWith(age: 31);

  // JSON serialization
  final json = user.toJson();
  final newUser = User.fromJson(json);
}
```

In summary, `Freezed` is a powerful tool for managing immutable data models in Flutter, reducing boilerplate code, enhancing type safety, and simplifying state management.
