# cordova-plugin-is-default-keyboard

Cordova plugin that provides JS API to check if custom keyboard is used on Android as well as blocking custom keyboards on iOS

## install

    cordova plugin add cordova-plugin-is-default-keyboard

## usage

#### Android
On Android `DefaultKeyboard` JS API is available with `isDefaultKeyboard(onSuccess(Boolean), onFailure)` method.
Example usage in React:

```
if (window.DefaultKeyboard) {
    const setIsDefaultKeyboard = isDefaultKeyboard => this.setState({ isDefaultKeyboard });
    DefaultKeyboard.isDefaultKeyboard(setIsDefaultKeyboard, error => {
        console.warn(error);
    });
}
```   

#### iOS
Application will not allow third party keyboards defaulting to system keyboard.