# Space Discovery AR — Group 56

An interactive marker-based WebAR museum made with HTML, A-Frame 1.3.0 and AR.js 3.4.5, following the lecturer's Basic AR Project Guide and AR Activity.

## Assignment requirement checklist

1. **Hiro marker scene:** four main exhibit objects (rocket, planet, satellite and space station), several different primitives, and 3D text labels.
2. **Animation:** rotating rocket, bouncing planet, rotating space station and an animated rocket launch/return.
3. **3D model:** original low-poly rocket in `models/space-rocket.glb`; it is not the workshop duck. A built-in primitive rocket fallback is displayed if the GLB fails to load.
4. **Interaction:** planet colour cycling, satellite grow/shrink, and rocket launch/return. Custom A-Frame components are used. On-screen HTML controls provide a backup for mouse/touch object interaction.
5. **Status banner:** changes on `markerFound` and `markerLost`.
6. **Hosting:** deploy the complete folder to a public HTTPS host (GitHub Pages or Netlify) and test on a phone.

## Project files

- `index.html` — complete WebAR application.
- `models/space-rocket.glb` — original low-poly 3D rocket model.
- `README.md` — setup, features and testing notes.

## Run on a laptop

1. Extract the ZIP.
2. Open the `Space_Discovery_AR_Group_Project` folder in Visual Studio Code.
3. Install the Live Server extension if it is not installed.
4. Right-click `index.html` and select **Open with Live Server**.
5. Allow camera permission in the browser.
6. Show the whole Hiro marker (including its black border) to the webcam.

## Interactions

- Click **LAUNCH ROCKET** to move the rocket upward; press **RETURN ROCKET** to bring it back.
- Click the planet or **CHANGE PLANET** to cycle through five colours.
- Click the satellite or **GROW SATELLITE** to enlarge/restore it.
- **RESET** returns the interactive objects to their initial states.
- On desktop, you can also click the 3D objects directly. On phones, use the on-screen controls if direct 3D tapping is difficult.

## Performance and compatibility notes

- The scene uses modest geometry and 640×480 camera input as a practical baseline for laptop and phone testing.
- Camera access requires `localhost` or HTTPS and browser permission.
- The A-Frame and AR.js libraries load from CDNs, so an internet connection is required.
- Marker tracking quality still depends on lighting, focus, camera quality, marker size and avoiding glare. No browser AR project can be guaranteed to work in every device or environment.

## Troubleshooting

- **Black camera view:** check camera permission; use Live Server or an HTTPS URL, not `file://`.
- **Marker not found:** show the full Hiro marker, keep it flat, improve lighting and reduce screen glare.
- **GLB not visible:** check that `models/space-rocket.glb` is present. If loading fails, the app displays a simple built-in rocket fallback.
- **Object click unreliable:** use the on-screen buttons; the controls trigger the same A-Frame custom components.
- **Changes not visible:** save the file and hard-refresh the browser (`Ctrl+Shift+R`).

## Original model credit

The low-poly rocket GLB was created specifically for this student project from primitive geometry. No third-party model asset is included.
