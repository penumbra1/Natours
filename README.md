This is my implementation of a study project for "Advanced CSS and SASS" course. Original design is by [Jonas Schmedtmann](https://twitter.com/jonasschmedtman) (an awesome teacher). Although I coded this project along with the course, I met my goal of building everything from scratch without referring to the source or missing a chance to improvise.

Here are some of my improvements to the codebase and the design:

## Typography & layout

- Lots of tiny tweaks: margins, padding, font-sizes, skew angles etc.
- Muli instead of Lato: I found its stroke width more consistent in all-caps titles, and its lower x-height looks more casual;
- New h2 hover animation: the original one seemed too striking, so I came up with a subtler "swing" and gradient displacement;
- Buttons: adapted hover animation to touch devices (e.g. box shadow is always visible, text buttons are flat and animated on touch etc.)
- Slightly changed the photo composition layout and animation to zoom well on all screen sizes
- Reshaped stories into columns on mobile screens
- Nav menu: on touch devices, button selection and menu close animations are triggered sequentially on tap instead of independently on hover+click
- Book popup layout: added a new responsive image and layout
- Booking form: made the diagonal gradient responsive, merged mutually exclusive radio options into a single checkbox
- Expanded responsive design to smallest phones (down to ~320px)

## Code

- Added a few mixins, variables and scoped functions for DRYer SASS (e.g. section layout, card gradients)
- Used flexbox for minor centering and responsiveness. Considering getting rid of clearfix completely.
- Tried to fix font rendering on Chrome for transformed elements (buttons, story avatars), but found no optimal solution and resorted to backface-visibility: hidden and filter: blur(0.0px) for now.
- Used [node-sass-watcher](https://www.npmjs.com/package/node-sass-watcher) to watch and autoprefix with a single npm script
- Little tricks like object-fit, transform-origin, text-indent etc.
