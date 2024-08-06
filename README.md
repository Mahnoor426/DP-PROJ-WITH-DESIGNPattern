## ZELDA GAME

## PROJECT OVERVIEW
The project is "Zelda," a text-based adventure game in which the player sets out on
a valiant mission to save Princess CPeria from a wicked wizard. Nine chambers
full of difficulties, treasure, and creatures make up the game. To save the princess
in the end, players will need to employ strategic thinking to find their way across
the rooms, knock out strong opponents, and obtain crucial items like a silver
dagger and a magical shield.

## DESIGN PATTERN ADDED 
## 1. STRATEGY DESIGN PATTERN
The Strategy design pattern is implemented in Zelda.cpp to define a family of
algorithms, encapsulate each one, and make them interchangeable. In this game,
different attack strategies are represented by classes such as ShieldAttack and
DaggerAttack. The Player class uses these strategies to perform attacks, allowing
it to switch between different attack methods dynamically. This pattern enhances flexibility, as new attack strategies can be added without modifying the Player
class, adhering to the open/closed principle. 

## 2. STATE DESIGN PATTERN
The State design pattern is employed in Zelda.cpp to manage the game states
dynamically. The GameState class is an interface for different states, with
subclasses like EndLoseState, PlayingState, and EndWinState providing
concrete implementations. These subclasses override methods such as Play(),
Move(), Pick(), Drop(), Look(), Attack(), Exit(), ChangeState(), and
LoseGame(), enabling state transitions based on player actions. This pattern
ensures player can easily transition between different states, making it more
manageable and maintainable.

## 3. FACTORY DESIGN PATTERN
The Factory design pattern is used across various factory classes, such as
TreasureFactory, WeaponFactory, MonsterFactory, PlayerFactory,
PrincessFactory, and CastleFactory. These factory classes encapsulate the
creation of game objects, such as treasures, weapons, monsters, players,
princesses, and castles, respectively. By delegating the instantiation process to
these factories, the game achieves a higher level of modularity. It decouples
object creation from their usage, promoting scalability and ease of modification.

## 4. SINGLETON DESIGN PATTERN
The Singleton design pattern is applied to the Game class to ensure that only one
instance of the game engine exists throughout the application's lifecycle. This is
achieved through a private constructor and a static method getInstance() that
returns the single instance. By managing the game state and progression through
a single instance, the pattern guarantees a consistent and centralized control
point, preventing potential conflicts and ensuring coordinated access to shared
resources.

