# Drum Kit 🥁

An interactive drum simulator that responds to keyboard presses, built with plain HTML, CSS, and JavaScript. This project was developed to practice DOM event manipulation and web audio playback.

![Project Background](Drums-Exercise/background.jpg)

## How It Works

The simulator uses JavaScript event listeners to detect when a key is pressed (`keydown`). Each key on the screen is associated with a specific `data-key`, which corresponds to a sound.

1. **Event Capture**: An event listener on the `window` captures the `keydown` event.
2. **Element Selection**: The event's `keyCode` is used to find the corresponding `<audio>` element and `<div>` key.
3. **Audio Playback**: The sound is rewinded (`currentTime = 0`) and then played using `.play()`.
4. **Visual Feedback**: A `.playing` class is added to the key's `<div>` to trigger a CSS transition.
5. **Effect Removal**: A `transitionend` event listener waits for the animation to finish before removing the `.playing` class, getting the system ready for the next interaction.

## Technologies Used

- **HTML5**: For the structure and semantics of the elements.
- **CSS3**: For styling and animations (`transition`).
- **JavaScript (ES6+)**: For the interactivity logic and DOM manipulation.

## How to Run the Project

1. Clone this repository.
2. Open the `index.html` file in your preferred browser.
3. Press the keys (A, S, D, F, G, H, J, K, L) to play the drum sounds.

## Project Structure

```
/
├── index.html
├── style.css
├── script.js
├── background.jpg
└── sounds/
    ├── clap.wav
    ├── hihat.wav
    ├── kick.wav
    └── ... (other audio files)
```
