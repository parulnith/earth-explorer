# Earth Explorer ✈️

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Twitter Follow](https://img.shields.io/twitter/follow/pandeyparul?style=social)](https://twitter.com/pandeyparul)

**Earth Explorer** is a 3D globe adventure for kids. Start from home in India, choose a wonder of the world, and fly there. A plane follows a real curved flight path across the globe, lands, and then you can explore the place in photorealistic 3D.

---

## 🎮 How it works

1. **Pick a starting city** (New Delhi, Mumbai, Bengaluru and more).
2. **Choose where to go.** Tap a wonder card, click a pin on the globe, type a name, or press 🎤 and say it, like *"Take me to the Eiffel Tower"*. Spelling slips are fine: *"efel tower"* works too.
3. **Fly there.** The plane takes off from a landmark in your home city, climbs out of the clouds, and the camera rises into space mid-flight to show the curved great-circle route, the shortest way around a round Earth. A captain talks you through the trip, and the ticket shows kilometres flown, height, and how long a real flight would take.
4. **Land and explore in 3D.** The plane descends through clouds and the camera swoops down to the real wonder in photorealistic 3D. Switch between circling it, a bird's-eye view and an up-close view, or drag and zoom yourself.
5. **Learn and collect.** Each wonder has three facts (read aloud if you like) and a quick quiz. Every visit adds a stamp to your passport.
6. **Keep going.** The next flight starts from where you are, so you can hop from Paris to Giza to Rome, then fly home.

## 🌍 Wonders included

Taj Mahal, Eiffel Tower, Great Pyramid of Giza, Colosseum, Great Wall of China, Machu Picchu, Christ the Redeemer, Chichén Itzá, Petra, Statue of Liberty, Sydney Opera House, Burj Khalifa, Mount Everest and the Grand Canyon.

To add your own, copy one entry in the `WONDERS` list in `earth_explorer.html`. Each entry holds its coordinates, a camera view, some aliases for search and voice, three facts and one quiz question.

---

## 🚀 Getting started

### 1. Get a free Cesium ion token

- Sign up at [ion.cesium.com](https://ion.cesium.com/).
- Go to **Access Tokens** and copy your default token.
- For photorealistic 3D cities, open the **Asset Depot** and add **Google Photorealistic 3D Tiles** to your account. Without it, the game falls back to Cesium OSM Buildings.

### 2. Add the token

Put it in `env.js` next to the HTML file:

```javascript
window.CESIUM_ION_TOKEN = 'your-token-here';
```

Add `env.js` to `.gitignore` so your token isn't committed. If `env.js` is missing, the game asks for a token on screen and remembers it in that browser.

If you host the game publicly (for example on GitHub Pages), the token has to ship with the page, so anyone can see it. Create a separate token for the public site and set its **Allowed URLs** in the Cesium ion dashboard to your site's address.

### 3. Run it

Voice input needs the page to be served, not opened as a file:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000/earth_explorer.html` in Chrome or Edge. Voice input needs one of those browsers; everything else works in any modern browser.

---

## 📚 Educational value

Kids practise world geography by choosing where to go. They see how far places are from home and why flights curve on a globe. They also explore landmarks up close instead of in a flat photo. It works for classrooms (put it on a projector and let the class vote on the next stop) or for exploring at home.
