# citygrid
An HTML-based city plan designer, inspired by D&amp;D dungeon designers. Coded with Claude Fable 5.2.
To use on your own computer, download index.html and then open with your browser.  The app opens with a sample city; press New for a blank plan. You can also download san-francisco.json and import the file to regenerate the sample map (San-Francisco.png) for yourself.

**Terrain background**
Import a PNG, JPEG or WebP image to sit under the grid. Move it with the "Move the image" tool, and adjust its size and opacity with the sliders. The zoning opacity slider controls how much the zone colors cover it.

**Natural features and resources**
- "Water body" and "Park / nature reserve" tools: draw a freehand outline and it closes into an area. Water is filled; a park is see-through with a thick green band inside its boundary. River or shoreline draws an open blue line that merges with any water body it meets. An outline of a body of water that starts and ends at the edge of the map is closed along the map border, so coastlines sit flush against the edge.
- "Land / island": draw an outline over water to cut that shape out of it, for an island or to push a shoreline back. Shapes apply in the order drawn, so drawing water over land floods it again.
- Resources (groundwater, farmland, forest, ore, oil): freehand regions shown as hatched overlays, each with its own pattern, so overlapping regions stay readable.
- Water bodies and rivers sit beneath the zoning, so they show through unzoned tiles or when zoning opacity is lowered. Parks and nature reserves are drawn over the zoning, and resource regions over those.
- Remove items using the "Erase a natural feature or resource area" tool. 
- Natural features and resources are in a single display layer, with show/hide toggles for each one and an opacity slider which covers both.

**Zoning**
- 24 zone types in seven groups: residential, commercial, office, industrial, mixed use, institutional and open land, plus Unzoned.
- Paint with Brush, Box (drag a rectangle) or Fill (flood a connected area).
- Each zone shows a live tile count. Type a target beside a zone to track progress: the "Left" column shows the tiles still needed, `0` in green when on target, and `+n` in red when over.
- Residential is a 3 × 3 grid of social class (working class, middle class, elite) by density (low, mixed, high). Shade shows class, from pale to dark green. Hatching shows density: none for low, single diagonal for mixed, cross-hatch for high.
- Two-letter zone codes appear on tiles when zoomed in. Residential codes give class then density, for example WH for working class, high density.

**Roads and transit**
- Roads: limited-access highway, proposed highway (dashed), major arterial, minor multi-lane road.
- Transit: railroad, subway (or elevated), streetcar (tram).
- Draw Freehand or Straight (drag from start to end). In Freehand, hold Shift for a straight line.
- Line ends snap to nearby lines of the same family. Streetcar lines are straightened and snap to the nearest 15°.
- Commercial strip buffer: drag along a major arterial or minor road to give that stretch a blue buffer marking it as a commercial strip. Remove a stretch with the "Erase part of a commercial strip buffer" tool.
- Stations and interchanges snap onto a matching line: highway interchange, rail station, subway station, streetcar stop.

**Civic stamps**
- Hospital, university, cemetery, golf course, zoo, amusement park, stadium, airport, rail or subway depot, seaport, ferry, landfill, power plant and waterworks. Tap to place, drag to move, and tap a stamp with the same stamp selected to remove it.

**Editing**
- Erase part of a line rubs out only the stretch you drag over. Erase a whole line removes the entire line. A single drag only affects one type of line.
Undo and redo: the buttons, or Ctrl/Cmd+Z and Ctrl/Cmd+Shift+Z.
- Zoom with pinch, the scroll wheel or the + and − buttons. Pan with right-click and drag; with two fingers, the Pan button in the top bar, or by holding Space and dragging.
- Tap a section heading in the tool tray to fold it away; the planner remembers which sections are open.

**Layer tools**
Terrain, zoning, roads, transit, civic stamps, and the underlying grid and row/column labels can all be shown or removed. 

**Plans, saving and export**
- Plans are stored in the browser on the device you are using. You can keep several named plans. Rename the open plan in the top bar; open, duplicate or delete plans under Plans. Clearing browser data removes your plans, and they are not shared between devices or people.
- "Save file" downloads the open plan as a JSON file. Import loads a JSON file as a new plan. Use these to back up a plan or move it to another device.
- Export PNG saves an image of the map with a scale bar and a legend of the natural features, resources, zones, lines, stations and stamps the plan uses.

**Notes**
- Fonts (Overpass and Public Sans) load from Google Fonts. Without a connection the app falls back to system fonts.
- Requires a current version of Chrome, Edge, Firefox or Safari.
- I wanted to get the idea for this tool and its implementation out into the world, but I don't intend to actively maintain it. Forks and further experimentation are welcome; maybe someone will retool this for Cities Skylines 1, for example, adding additional stamps and other features based on its DLC and features.

