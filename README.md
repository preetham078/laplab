# Laptop Lab: 3D Laptop Customizer and Hardware Simulator

An interactive 3D laptop studio that runs in the browser. Open the lid, look inside, lift out the RAM, swap the SSD and see which parts are soldered for good. Every component is its own selectable 3D object.

> **Status:** early release (phase 1). The homepage and the 3D studio work today. The builder dashboard, performance simulator and other modules are on the roadmap below.

## Features

**Homepage**
- Dark, futuristic interface with an animated 3D laptop in the hero
- Start building and Explore hardware buttons that jump into the studio
- Storage comparison table
- Recent configurations section with sample builds

**3D laptop studio**
- Rotate 360 degrees, zoom, and use Front, Top, Side, Rear and Reset views
- Open and close the lid with a button or a slider
- Exterior and internal views
- Exploded view that separates every component
- Click a part (or pick it from the parts list) to highlight it and see its specifications
- 16 separate objects: CPU, GPU, RAM, SSD, HDD, motherboard, cooling fan, heat pipes, battery, speakers, display and lid, keyboard, trackpad, Wi-Fi card, ports, chassis

**Hardware replacement**
- Remove RAM, SSD, HDD, battery, Wi-Fi card or cooling fan and watch the part lift out of its slot
- Choose a replacement, see it drop back in, and watch the build summary update
- Soldered parts (CPU, GPU) are clearly marked as not upgradeable, with an explanation
- Incompatible options are disabled with the reason shown (for example, a 99 Wh battery cannot be used while the 2.5″ HDD bay is occupied)

**Builds**
- Save a build, reset it, and reload any saved or sample build into the 3D view

## Controls

| Action | Input |
| --- | --- |
| Rotate | Drag |
| Zoom | Scroll, or the + and − buttons |
| Select a part | Click it, or choose it from the Parts list |
| Remove a part | Select a removable part, then Remove component |
| Replace a part | Choose an option from the replacement list |
| Internal view | Toolbar: Internal view |
| Exploded view | Toolbar: Exploded view |

## Tech stack

- HTML, CSS and JavaScript in a single file (`index.html`)
- [three.js](https://threejs.org/) r128 (loaded from cdnjs)
- Chakra Petch (Google Fonts)

## Project structure

```
laptop-lab/
├── index.html   # homepage, 3D studio, hardware data and compatibility rules
└── README.md
```

## Roadmap

- [ ] Custom builder dashboard (Intel Core i3, i5, i7, i9 and AMD Ryzen, GPU, RAM, storage, display, battery, cooling)
- [ ] Performance simulator with charts, clearly labelled as estimates
- [ ] Before and after comparison with estimated upgrade cost
- [ ] Hardware Knowledge Center with interactive diagrams
- [ ] Rename, compare and export saved configurations (JSON and PDF)
- [ ] User accounts and persistent saved builds with Supabase
- [ ] Photorealistic GLB models with PBR materials, HDRI lighting and post-processing
- [ ] Migration to React, TypeScript, Tailwind CSS and React Three Fiber

## Known limitations

- Components are drawn in code from basic shapes, textures and bevels. They are not photorealistic, and real GLB models are planned.
- Saved builds live in memory and are lost when the page is reloaded.
- Compatibility rules and specifications are simplified for the simulation.

## Disclaimer

Laptop Lab is a simulation. Specifications, compatibility rules and any estimates are simplified illustrations. They are not benchmark results, manufacturer data or real hardware testing.

## Contributing

Issues and pull requests are welcome. For larger changes, please open an issue first to discuss what you would like to change.

## License

MIT. Add a `LICENSE` file with your name and the year before publishing.

## Credits

- [three.js](https://threejs.org/) for 3D rendering
- [Chakra Petch](https://fonts.google.com/specimen/Chakra+Petch) by Cadson Demak
