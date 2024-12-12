# Gridlock Rush: A Car Simulator Game

## Game Overview

**Gridlock Rush** is an engaging car simulation game where players navigate through challenging traffic scenarios. Test your driving skills, solve puzzles, and experience the thrill of overcoming gridlocks in style.

![Gridlock Rush Banner](./Project-Images/Symbol_3.jpg)

## Key Features

- **Low-Poly Style**  
  A charming and visually appealing low-poly art style designed for mobile platforms.

- **Easy and Fun Gameplay**  
  Enjoy an intuitive, easy-to-learn driving experience that’s perfect for players of all ages.

- **Realistic Traffic Simulation**  
  Navigate through dynamically changing traffic conditions while solving fun and engaging challenges.

- **Time Trial Mode**  
  Race against the clock to complete levels as quickly as possible, testing your driving skills under pressure.

- **Level System**  
  Progress through levels with increasing difficulty, unlocking new challenges and rewards as you advance.

- **Intuitive Controls**  
   Simple, responsive controls that make it easy for players to jump right in and enjoy the game.
  ![Key Features Screenshot](path/to/features-screenshot.png)

## Game Details

- **Title**: Gridlock Rush
- **Version**: 1.0.0
- **Platform**: Android
- **Developer**: OPCD STUDIO
- **Release Date**: Coming soon on the Play Store!

## Code Review

Before diving into the gameplay and visual insights, a thorough **Code Review** is essential to ensure quality, maintainability, and performance of the game.

1. **Code Structure**:

   - Ensure that the project is organized in a clear and logical structure with separate directories for assets, scripts, and resources.
   - Avoid unnecessary code duplication and ensure modularity.

2. **Performance Optimization**:

   - Optimize traffic simulations and physics calculations for better performance on mobile devices, aiming for a smooth experience across various Android devices.
   - Analyze memory usage and ensure the game runs efficiently under load (multiple vehicles on screen).

3. **Error Handling and Debugging**:

   - Thoroughly test major gameplay features such as traffic AI, car physics, and player interactions to ensure there are no major bugs.
   - Debug any existing issues, particularly with timing, physics, or user input.

4. **Code Readability**:

   - Ensure the code is clean, well-documented, and follows standard practices for readability.
   - Use meaningful variable names and clear comments to make it easier for future developers to contribute.

5. **Testing**:
   - Write unit tests for key features like traffic behavior, car controls, and game mechanics.
   - Stress-test the game with various scenarios to ensure smooth performance and bug-free gameplay.

### Use of PlayerPrefs in `LevelManager` Script

In the **`LevelManager`** script, we use **`PlayerPrefs`** to manage the progression of the levels the player has unlocked. Here’s an explanation of how **`PlayerPrefs`** is used:

```csharp
int levelsUnlocked = PlayerPrefs.GetInt("levelsUnlocked", 1);
Debug.Log("Levels Unlocked: " + levelsUnlocked);

foreach (Button button in buttons)
{
    button.interactable = false;
}

for (int i = 0; i < levelsUnlocked && i < buttons.Length; i++)
{
    buttons[i].interactable = true;
    Debug.Log($"Button {i} is interactable.");
}
```
