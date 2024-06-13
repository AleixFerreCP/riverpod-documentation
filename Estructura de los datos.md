La estructura de archivos va a ser la siguiente (reemplaza `pokemon` por el nombre de la feature en cuestión):

`/pokemon`
	- `/widgets`
		- `pokemon_widget.dart` How it needs to look, it listens to the provider
	- `/models`
		- `pokemon_model.dart` How the data is structured
	- `/repositories`
		- `pokemon_repository.dart` All the http logic
	- `/providers`
		- `pokemon_provider.dart` How it needs to treat the info from the repo
		- `(pokemon_notifier.dart)` If it needs more provider types


## Flow de los datos
 -> widget hace watch del provider -> el provider llama al repository -> el repository hace la request http -> el provider recibe la info del repository y mantiene logica de los datos que recibe -> se lo envia al widget desde el watch y este lo renderiza en el build method.

## Models
Los models son la estructura de los datos, también puede tener `factory` para crear constructores custom.