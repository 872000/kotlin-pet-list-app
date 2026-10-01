# Kotlin Pet List

An Android app in Kotlin that displays a list of pets in a scrollable card list. Each pet is a `Pet` data class (name, vaccination flag, age, and kind — cat, dog, or rabbit), rendered as a rounded card in a Compose `LazyColumn`. A `PetViewModel` holds the list as Compose state and the `PetList` screen observes it.

## Tech stack

- Kotlin
- Jetpack Compose (Material 3)
- AndroidX Lifecycle ViewModel
- compileSdk 33 / minSdk 31

## Project structure

```
app/src/main/java/Pet.kt               Pet data class + Kind enum (CAT, DOG, RABBIT)
app/src/main/java/PetViewModel.kt      ViewModel exposing the pet list as MutableState
app/src/main/java/PetList.kt           LazyColumn list + PetRow card composable
app/src/main/java/.../MainActivity.kt  hosts PetList via the ViewModel
app/src/main/java/.../ui/theme/        Compose theme (colors, typography)
```

## Build & run

```bash
./gradlew assembleDebug
# then install app/build/outputs/apk/debug/app-debug.apk on an emulator or device
```

Note: the sample data in `PetViewModel` is hard-coded placeholder data — the "pet names" are CPU model names (e.g. `i7-11800H`), never wired up to real data. The app compiles and renders the list as-is.
