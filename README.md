# Pets Adoption App 🦄

![Ipets](https://user-images.githubusercontent.com/84308096/167295237-ac5ea80c-cb66-4975-9a93-c844dbfc6b37.png)

## Instructions

- Fork and clone [this repository](https://github.com/JoinCODED/Task-Flutter-Get-AdoptApp-Button) to your `Development` folder.
- Endpoints:

```
Get pets, type: Get, https://coded-pets-api-crud.eapi.joincoded.com/pets
Create a new pet, type: Post, https://coded-pets-api-crud.eapi.joincoded.com/pets
Update a pet, type: Put, https://coded-pets-api-crud.eapi.joincoded.com/pets/{petId}
Delete a pet, type: Delete, https://coded-pets-api-crud.eapi.joincoded.com/pets/{petId}
Adopt a pet, type: Post, https://coded-pets-api-crud.eapi.joincoded.com/pets/adopt/{petId}
```

### Part 1: Get Data

1. Install `dio` into your project:

```shell
flutter pub add dio
```

2. Create a folder named `services`, inside it create a file called `pets.dart`.
3. Import `dio` package in `pets.dart`.

```dart
import "package:dio/dio.dart";
```

4. Create a new `DioClient` class and initialize a new dio instance.
5. Define your `_baseUrl`.
6. Create your first request that return a future list of pets and name it `getPets`.
7. Our endpoint is:

```
Get, http://http://10.0.2.2:5000/pets
```

8. Store the response of the request in a `Response` object.
9. Map your response to `Pet` objects using the `Pet.fromJson` constructor.
10. Don't forget to convert the result to a `List`.
11. Return your new `List` of `Pet`s.
12. Don't forget to wrap your request in a `try-catch` block.

13. In your `PetsProvider`, create a new function that returns a future void.
14. Import `services/pets.dart` file, and call `DioClient().getPets()` function, don't forget to `await`.
15. Lastly assign the result of `DioClient().getPets()` to the `pets` variable in the provider and call `notifyListeners`.

16. Create a button in your `home_page.dart` and call the provider method `getPets`. Don't forget to set `listen` to `false`.
