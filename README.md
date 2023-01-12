# Sample Problem Statement:
Student developers face problems regarding getting good developer resources, getting connected with their fellow developers, and getting opportunities. 
“Feel free to add the problems you face as a developer.”

# Screenshots:

<img width="721" alt="Screenshot 2022-10-10 at 12 36 40 AM" src="https://user-images.githubusercontent.com/61946155/194775840-feb0ff31-54c1-4f05-80f6-02ed6c9dc39a.png">

<img width="692" alt="Screenshot 2022-10-10 at 12 45 57 AM" src="https://user-images.githubusercontent.com/61946155/194775844-a249acdf-9731-4b3b-a0eb-f352b5476f3c.png">



# Sample Proposed Solution:
This project proposes a “Styava.dev Developer Community App” (Prototype) so that developers can interact with other fellow developers, get good developer resources, get updates about upcoming events, and join different developer communities.
“Feel free to suggest some more features that you think are required as a Developer.”

# Sample Functionality & Concepts used:
The App has a very simple and interactive interface which helps the students select the upcoming event. 
## Following are few android concepts used to achieve the functionalities in app:
## Constraint Layout : 
Most of the activities in the app uses a flexible constraint layout, which is easy to handle for different screen sizes.
Simple & Easy Views Design : Use of familiar audience EditText with hints and interactive buttons made it easier for students to register or sign in without providing any detailed instructions pages. Apps also use App Navigation to switch between different screens.
## RecyclerView : 
To present the list of different communities use the efficient recyclerview. 
## Google Maps API : 
You can also use the Google Maps API free version to get connected with local developer communities.
## LiveData & Room Database : 
You can use LiveData to update & observe any changes in developer events received from their mobile at real time and update it to local databases using Room. 

# Sample Application Link & Future Scope:
The app is currently in the Alpha testing phase and tested in the “STYAVA.DEV” community with a limited no. of users. 
You can access the app : [YOUR APP LINK HERE] (either Github link or Google Play store link of published app or .apk file).
Once the app is fully tested and functional in (your college / organization name), 
we plan to talk to neighboring communities also to propose this app idea and collaborate with them on this community app.


## Gradle Setup 

This template is using [**Gradle Kotlin DSL**](https://docs.gradle.org/current/userguide/kotlin_dsl.html) as well as the [Plugin DSL](https://docs.gradle.org/current/userguide/plugins.html#sec:plugins_block) to setup the build.

Dependencies are centralized inside the Gradle Version Catalog in the [libs.versions.toml](gradle/libs.versions.toml) file in the `gradle` folder.

## Static Analysis 

This template is using [**detekt**](https://github.com/detekt/detekt) to analyze the source code, with the configuration that is stored in the [detekt.yml](config/detekt/detekt.yml) file (the file has been generated with the `detektGenerateConfig` task). It also uses the **detekt-formatting** plugin which includes the ktlint rules (see https://detekt.dev/docs/rules/formatting/).

## CI 

This template is using [**GitHub Actions**](https://github.com/cortinico/kotlin-android-template/actions) as CI. You don't need to setup any external service and you should have a running CI once you start using this template.

There are currently the following workflows available:
- [Validate Gradle Wrapper](.github/workflows/gradle-wrapper-validation.yml) - Will check that the gradle wrapper has a valid checksum
- [Pre Merge Checks](.github/workflows/pre-merge.yaml) - Will run the `build`, `check` and `publishToMavenLocal` tasks.
- [Publish Snapshot](.github/workflows/publish-snapshot.yaml) - Will publish a `-SNAPSHOT` of the libraries to Sonatype.
- [Publish Release](.github/workflows/publish-release.yaml) - Will publish a new release version of the libraries to Maven Central on tag pushes.

## Publishing 

The template is setup to be **ready to publish** a library/artifact on a Maven Repository.

For every module you want to publish you simply have to add the `publish` plugin:

```
plugins {
    publish
}
```

## Project Structure

The project includes three sub-projects, each in their own subdirectories:

- **`app`:** The source for the final Android application.
- **`library-android`:** The source for an Android library including UI.
- **`library-kotlin`:** The source for a UI-less Kotlin library.
- **`library-compose`:** The source for a UI library with Jetpack Compose library.

The following additional top-level directories configure & support building the app & projects:

- **`buildSrc`:** Contains shared Gradle logic as [precompiled script plugins](https://docs.gradle.org/current/userguide/custom_plugins.html#sec:precompiled_plugins)
- **`config`:** Contains the [Detekt configuration file](https://detekt.dev/docs/introduction/configurations/).
- **`gradle`:** Contains Gradle Configuration files such as the Gradle Version Catalog and the [Gradle Wrapper](https://docs.gradle.org/current/userguide/gradle_wrapper.html).

Finally, the following hidden top-level directories provide functionality for specific development systems:

- **`.github`:** Defines the [Github Actions](https://github.com/features/actions) CI tasks and templates for new pull requests, issues, etc.
- **`.idea`:** Sets common initial project settings when the project is opened in [Android Studio](https://developer.android.com/studio) or [IntelliJ IDEA](https://www.jetbrains.com/idea/).

## Contributing 🤝

Feel free to open a issue or submit a pull request for any bugs/improvements.
