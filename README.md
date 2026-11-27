# Browser Whiteboard

A browser-based drawing surface built with React and the HTML Canvas API. It supports freehand sketching, geometric shapes, annotations, basic editing history and PNG export.

## Features

- Freehand brush using `perfect-freehand`
- Line, rectangle, circle and arrow tools
- Eraser and text annotation tools
- Configurable stroke color, shape fill and drawing/text size
- Undo and redo controls, with `Ctrl+Z` and `Ctrl+Y` keyboard shortcuts
- Export the current canvas as a PNG image

## Tech stack

- React 18 and Create React App
- HTML Canvas 2D API
- Rough.js for hand-drawn geometric shapes
- perfect-freehand for smooth brush strokes
- React Context and reducers for board/tool state
- CSS Modules and React Icons

## Run locally

Requires Node.js and npm.

```bash
git clone https://github.com/sachin2967/whiteboard.git
cd whiteboard
npm install
npm start
```

The app runs at [http://localhost:3000](http://localhost:3000).

Create a production build with:

```bash
npm run build
```

## How it is organized

```text
src/
  components/
    Board/       Canvas rendering and mouse interaction
    Toolbar/     Tool selection, undo/redo and PNG export
    Toolbox/     Color, fill and size controls
  store/
    BoardProvider.js
    ToolboxProvider.js
  utils/
    element.js   Shape generation and hit testing
    math.js      Geometry helpers
  constants.js   Tool and action definitions
```

## Scope and limitations

This is a client-side drawing application. Board state is held in browser memory; there is no backend, multi-user collaboration, automatic cloud save or project persistence. Export the board before refreshing or closing the page. The current canvas event handlers are mouse-based, so touch and stylus behavior has not been verified.

## License

No license is currently specified. All rights remain with the copyright holder unless a license is added.
