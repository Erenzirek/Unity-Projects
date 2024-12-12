# Unity Quit Application Script

This script provides functionality to quit the application in Unity. It is particularly useful for adding a "Quit" button in your game's UI.

## Code Example

```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

// Manages application quit functionality
public class NewBehaviourScript : MonoBehaviour
{
    // Quits the application when invoked
    public void QuitApplication()
    {
        // Initiates the application exit process
        Application.Quit();

        // Logs a message indicating the quit process was triggered
        Debug.Log("Exit initiated");

        // Specific to Unity Editor: Stops play mode
        #if UNITY_EDITOR
        UnityEditor.EditorApplication.isPlaying = false;
        #endif
    }
}
```

## Key Features

- **Application.Quit()**: Initiates the application shutdown.
- **Debug.Log()**: Outputs a message to the console for debugging purposes.
- **Editor-Specific Behavior**: Ensures the functionality works within the Unity Editor by stopping play mode.

## Usage

1. Attach this script to a GameObject in your Unity scene.
2. Create a UI button in your scene.
3. Assign the `QuitApplication` method to the button's `OnClick` event in the Inspector.

## Notes

- **Build and Play**: The `Application.Quit()` method only works in a built game. It does not function within the Unity Editor.
- **Editor Compatibility**: The `UnityEditor.EditorApplication.isPlaying` line ensures testing convenience within the Unity Editor.
- **Debugging**: The `Debug.Log()` line can be removed or commented out in production builds.

## Example Scenario

Add a "Quit" button to the main menu of your game and link the `QuitApplication` method to provide players with a way to exit the game.
