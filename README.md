# MAP v1 – Make A Pack

*Pokendy Intern Tool*

Classify Pokémon card images by rarity and download them with organised file names.

---

## Features

| Feature                       | Description                                                                                                            |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Real‑time preview             | Displays the current card (PNG) in the browser.                                                                        |
| One‑click classification      | Buttons Normal / Rare / High / Ultra (keyboard shortcuts **A, Z, E, R**) save the card with the appropriate file name. |
| PNG to JPG conversion         | Automatically converts the downloaded image to JPG to reduce file size.                                                |
| Progress indicator            | Native HTML `<progress>` element with “current / total” text.                                                          |
| Skip                          | Advances to the next image without downloading the current one.                                                        |
| URL parameters                | `packName`, `maxIndex`, `_padStart` to target any set and manage zero‑padding.                                         |
| Metadata fetch (experimental) | Prototype for retrieving card information from *pikawiz.com*.                                                          |

---

## Quick start

```bash
git clone https://github.com/TrixProduction/pit-map-v1
cd map-v1
```

No external dependencies: open `index.html` in your browser.

Example:

```
file:///.../pit-map-v1/map/index.html?packName=celestialstorm&maxIndex=245&_padStart=3
```

If parameters are missing, the page runs with an example set and reminds you of the correct syntax.

---

## Usage

1. **Select or configure a set**

   | Key         | Description                                            | Example          |
   | ----------- | ------------------------------------------------------ | ---------------- |
   | `packName`  | Folder on `https://www.pikawiz.com/images/{packName}/` | `celestialstorm` |
   | `maxIndex`  | Total number of cards in the set                       | `245`            |
   | `_padStart` | Length of the zero‑padded index                        | `3` → `001.png`  |

2. **Classify**

   * Click a rarity button or press its keyboard shortcut.
   * The file is downloaded as `1.jpg`, `1000.jpg`, `10000.jpg`, `9990.jpg`, then `2.jpg`, `1001.jpg`, etc., depending on the selected rarity.

3. **Skip**

   * Use the **SKIP** button to move to the next card without downloading.

---

## Customisation

| Change             | Location                                  | Notes                                   |
| ------------------ | ----------------------------------------- | --------------------------------------- |
| Rarity ranges      | `downloadCounts` object and button labels | Adjust starting values or labels.       |
| Theme and colours  | `<style>` section                         | Modify gradients, border‑radius, fonts. |
| Keyboard shortcuts | `buttonMappings` object                   | Map different keys.                     |

---


## License

Released under the MIT License.

Pokémon images and trademarks © The Pokémon Company / pikawiz.com.

---

## Credits

Developed by the Pokendy team.

Font: Ubuntu, Google Fonts.
