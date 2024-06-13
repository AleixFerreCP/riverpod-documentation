The file structure will be as follows (replace `pokemon` with the name of the feature in question):

- `/pokemon`
  - `/widgets`
    - `pokemon_widget.dart` - How it needs to look, it listens to the provider.
  - `/models`
    - `pokemon_model.dart` - How the data is structured.
  - `/repositories`
    - `pokemon_repository.dart` - All the HTTP logic.
  - `/providers`
    - `pokemon_provider.dart` - How it needs to handle the info from the repository.
    - `(pokemon_notifier.dart)` - If it needs more provider types.

## Data Flow

-> The widget watches the provider -> the provider calls the repository -> the repository makes the HTTP request -> the provider receives the info from the repository and maintains the logic of the received data -> it sends the info to the widget through the watch, and the widget renders it in the build method.

## Models

The models are the structure of the data, and they can also have a `factory` to create custom constructors.
