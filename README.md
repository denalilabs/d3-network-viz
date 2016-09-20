# Visualization using d3 force layout

Research notes for a data visualization consulting project - http://denalilabs.github.io/d3-network-viz/

# Background
The d3 force layout is a physical simulation, that mainly relies on repulsive charges and center of gravity to control its behavior. There is an inherent randomness in the resulting layout, which seems like a good choice for infographic designs. However there are a few side-effects of this choice that you should be aware of:

## Issues: Animations
The animation of nodes is controlled by the forces of charge, gravity, friction and alpha. If those variables are not sufficient for animation needs, we need to override the default positioning algorithm. This is necessary if you need precise control of node movement (ex: moving node to a particular place to show description).

## Issues: Overlapping nodes
The random movement of nodes may cause overlapping with other nodes or HTML elements. Although there are methods to avoid collision with SVG nodes, a custom plugin would need to be written for html collisions. This is necessary if you want to avoid overlapping nodes with heading, description and radio buttons within its space.

## Issues: Single page
The infographic can feel structured and consistent, if it all happens on a single page. Navigating to a different page may have a jarring effect. However, single page design requires extra logic to handle urls. This is necessary if you want to allow direct access to individual pages.
