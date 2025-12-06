# MiniPets
# Overview:
**Platform Focus Area**

This tutorial of MiniPets explores building an Adriod app with Jetpack Compose with a focus on Game Development.

We will be going thorugh this demo game called MiniPets, a virtual pet simulator where the player cares for and interacts with a digital cat 🐱. The app demostrates core game development concepts adopted to Andriod without relying on traditional engines like Unity.  

# Getting Started:

**Required Software**

- Andriod Studio
   
   MiniPets is built using Jetpack Compose, which a more recent version of Andriod Studio. So we recommend       the version Andriod Studio Koala or newer. You can download it here https://developer.android.com/studio

- Andriod SDK Components

  Required compenents:
    - Andiod SDK Platform 34 (or newer)
    - Andriod SDK Build-Tools
    - Andriod Platforms-Tools

- Project Dependencies

    MiniPets uses Jetpack Compose and other Andriod Libraries to manage the UI, state, and navigation. Your       project will need the following dependencies:
    - implementation("androidx.compose.ui:ui:<version>")
    - implementation("androidx.compose.material3:material3:<version>")
    - implementation("androidx.compose.ui:ui-tooling-preview:<version>")
    - debugImplementation("androidx.compose.ui:ui-tooling:<version>")
    - implementation("androidx.navigation:navigation-compose:<version>")
    - implementation("androidx.lifecycle:lifecycle-viewmodel-compose:<version>")
    - implementation("org.jetbrains.kotlinx:kotlinx-coroutines-android:<version>")
    - implementation("org.jetbrains.kotlinx:kotlinx-serialization-json:<version>")

# Coding Instructions:

To build the MiniPets game, the first step was to establish core game logic. We did this by mapping out each page and what would be needed in the ViewModel. This included pet's statistics (like happiness, energy, and coins), the player and pet names, temporary messages that show as popups to the player, and the cat's position in the environment. The viewmodel is also equipped to handle timed event, like the clearing of popup messages and moving the pet around the room. 

One the game logic wass in place, we built the main gameplay screens. This included the main screen where the user can use the action buttons (like Walk, Nap, Play) as well as watch their pet move around the room. The pet's wandering behavior is represented visually by offsetting its position, allowing it to appear as if it is moving around the room. 

There are three additional screens, Profile, Store, and Info. The Profile screen's main functionality is to allow the player to update and edit their display information. The Store's main purpose allos players to spend the coins they earn in the world as well customize their pet's bedroom! The Info screen provides basic app overview, such as our mission statement and instructions on how to play.

The individual screens are connected through Navigation Compose. By navigating through the screens this mirrors the concept of game areas commonly found in game design. Once the navigation is in, the entire game because an interactive loop. The player's pet can move, players can upgrade their pet's bedroom, and players can interact with their pet to earn coins!


# Further Discussion & Conclusions

In this project, we built MiniPets, a virtual-pet style Android application developed using Kotlin and Jetpack Compose in Android Studio. Instead of using traditional Android Views or a game loop, MiniPets relies entirely on state-driven UI, ViewModels, and Composable functions to simulate “game-like” behavior.
Throughout the app, the primary game mechanics, such as updating pet stats, earning coins, and interacting with the store, are implemented using Compose state and coroutines inside the MiniPetsViewModel. This reactive approach means the UI automatically updates whenever the data changes, creating a smooth and responsive gameplay experience without needing a dedicated game engine.
What the Project Demonstrated

1. State-Driven Game Logic With ViewModels
   
The MiniPetsViewModel is the core of the game. It controls:

    •    Pet happiness
    
    •    Coin count and updating player stats
    
    •    Inventory
    
This demonstrated how Compose encourages you to keep game or app logic separate from drawing/UI code—an important principle for scalable Android development.

2.  Multi-Screen Navigation With a Route System
Using a simple Route sealed class and NavHost, you implemented:

    •    A Main Page
    
    •    A Store Page
    
    •    A Profile Page
    
    •    An Info Page
    
This showed how Compose Navigation allows developers to build small “game worlds” with multiple screens and structured UI flows.

3. Jetpack Compose UI Instead of a Game Engine
Our app uses Composables like:
Column()
Row()
Image()
Button()
This illustrates how Compose can support lighter, interface-driven games without needing the help of physics engines or 2D rendering frameworks.

4. Store & Inventory Mechanics
   
StoreViewModel and StorePage.kt implement:

    •    Available items
   
    •    Purchase logic
   
    •    Coin validation
   
    •    Updating the MiniPetsViewModel after successful purchases
   
This structure mirrors how many real games separate economy logic from core gameplay logic.

**Alternative Approaches & Potential Expansions**

While Jetpack Compose is a great choice for your type of virtual-pet game, developers may also consider alternative approaches depending on complexity:

If building a heavier or animated 2D game:

    •    Unity or Godot (robust 2D/3D engines)
    
Additions you could implement next:

    •    Sound effects for interactions
    
    •    Achievements, mini-games, or daily rewards
    
    •    Multiple pets or evolutions

**Final Thoughts**

MiniPets demonstrates that game concepts don’t always require a game engine. Using only Kotlin, Compose, and clean architecture, we implemented:

    •    A functional pet simulator
    
    •    Interactive UI screens
    
    •    A real store system
    
    •    Persistent simulation logic with ViewModels
    
It’s a great foundation that shows how modern Android tools can be used to produce playful, interactive experiences while keeping code modular, testable, and easy to extend.

# GitHub Source Code

All of our pixel art was hand draw by the amazing Leah using https://www.piskelapp.com/
