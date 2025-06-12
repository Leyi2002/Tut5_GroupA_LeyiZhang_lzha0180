# Tut5_GroupA_LeyiZhang_lzha0180
# Audio-Reactive Animation – Individual Submission

## How to Interact with the Work

1. Open `index.html` in your browser  
2. Click anywhere on the canvas to enable audio playback  
3. Wait for the music to begin – the entire artwork will begin **shaking**  
4. Move the mouse to control **volume and stereo channels**  

---


I chose **"Audio: Use the level or frequency content of an audio track to animate work"** as my personal task.

- I made patterns in **different quadrants** scale in response to audio levels.
- I added **mouse-controlled stereo panning and volume**, allowing interactive manipulation of sound output.
- I chose to make the **entire image respond organically** to sound, focusing on rhythm, immersion, and pulse.

## Inspiration

My visual inspiration came from:

1. **Van Gogh’s Starry Night** visualization animations  
2. **Surreal audio-reactive visual artworks** found in real-time music visualizers  

These references inspired me to make the artwork “breathe” – turning static visuals into living, music-synced forms.

---

## Technical Explanation

I used the `p5.sound` library to load and play an `.mp3` file and analyzed volume using `p5.Amplitude`. The core logic:

```js
let level = amplitude.getLevel();
let scaleFactor = map(level, 0, 0.5, 1, 1.3);
let shake = map(level, 0, 0.5, 0, 10);
```

- `scaleFactor`: causes overall scaling of canvas based on loudness  
- `shake`: causes canvas jitter using `random(-shake, shake)`  
- Mouse movement influences `song.setVolume()` and `pan()`  

### Changes Made to Group Code

- Added audio loading via `preload()`  
- Added amplitude and audio analysis in `draw()`  
- Injected rhythm-based effects into existing quadrant visuals  
- Did not alter layout, composition, or core design from the group image

## Difference from Group Members

- Mine responds **only to audio**. 
- I used **sound volume and rhythm** to animate shapes and control their energy  
- I incorporated **audio interactivity (mouse-driven pan/volume)** which others did not  

## External Resources & References

- [p5.sound documentation](https://p5js.org/reference/#/libraries/p5.sound)  
- [Starry Night animation (YouTube)](https://www.youtube.com/watch?v=kq4lf2rswEw)  
- [Audio visual inspiration](https://www.youtube.com/watch?v=Ph1SEFWcL58)  
- Background music: [Pixabay Royalty-Free Music](https://pixabay.com/music/)  

