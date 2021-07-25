### How To Use:

The **GamepadHelper** class in **gamepadhelper.js** can be copied into any project and imported as a module and used by calling the ```GamepadHelper.update()``` method within the game loop (see **game.js** for a simple example).

When a button on a connected gamepad is pressed or released, an event (**gamepadbuttondown** or **gamepadbuttonup**) will be dispatched to the document containing the respective indexes of the gamepad and button that was pressed in the **detail** property. Here is an example event listener that simply logs the gamepad/button that was pressed down:

```
document.addEventListener('gamepadbuttondown', (event) => {
    console.log(event.detail.gamepad, event.detail.button);
});
```

The current state of any button or axis on a connected gamepad can also be queried via the ```getButtonValue(gamepad, button)``` and ```getAxisValue(gamepad, axis)``` methods.

See the following for more info on the Gamepad API:
- https://www.w3.org/TR/gamepad/)[https://www.w3.org/TR/gamepad/
- https://developer.mozilla.org/en-US/docs/Web/API/Gamepad_API/Using_the_Gamepad_API
