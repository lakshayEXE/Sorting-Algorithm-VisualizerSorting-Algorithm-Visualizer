# Sorting-Algorithm-Visualizer
This is a progressive web app built using React and is used to visualize classic sorting algorithms such as insertion sort, merge sort, quick sort, heap sort, etc.

## Purpose
I wanted to improve my skills with React and also learn classic sorting algorithms. This project turned out to be a great way to achieve both of the aforementioned objectives at the same time.

## The `src` folder contains three subdirectories:

- `algorithms - Each sorting algorithm is contained in its own file and imports helper functions from the helpers.js file, which is also present inside this folder. Each algorithm file has two named exports and a default export. The named exports are <AlgorithmName>Key which returns a mapping of the color group and its meaning in the context of the algorithm, and <AlgorithmName>Desc which returns an object containing the description and details of the algorithm. The default export, AlgorithmName is a function that takes in an array of numbers, sorts it and returns an object that contains every state change that the array has undergone. This object is used to create the animation.

- _settings - This folder contains the the CSS files that only contain CSS custom properties declarations (also known as CSS variables) for the entirety of the app. These files are used to determine the overall look and feel of the application as all components rely upon these variables.

  - components - This folder is broken down into atoms, molecules and organisms subfolders as described in Brad Frost's Atomic Design.
  - The Atoms folder contains the smallest elements that are repeatedly used throughout the app - buttons, switches, backdrops, etc.
  - The Molecules folder contains more complex components that are used independently or as part of an organisms.
  - The Organisms folder contains components which are self contained sections of the app - the top bar, the visualizer, the app drawer, etc.
  - A case can be made for a component to be in either a molecule or organism. In these sorts of situations, I did not use an exact set of rules but rather left it to intuition.

- Each component is contained in its own folder and has 2 files. The index.js file contains the JavaScript code for the component and the style.css file contains rules for classes which are written using an alternate style naming scheme of BEM that is described as follows:

  - Blocks are written in PascalCase and must match the name of the corresponding component.
  - Elements are also written in PascalCase and separated from the block using double underscores (__). eg. ComponentName__ElementName.
  - An element is always part of a block, not another element.
  - Modifiers are written in lowercase.
  - The modifier name is separated from the block or element name by a single underscore (_). eg. ComponentName_modifiername_modifiervalue
