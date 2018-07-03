== Intro == Everyone knows that a coordinate system is in place to
navigate through the Runescape world. That coordinate system is based
off upon three variables, the Absolute X, Y Z coordinates. Before we
continue to talk about how these three variables are used in
calculations lets set down some vocabulary:

== Definitions == ===Tile=== A tile is a representation of an absolute
coordinate.

''Example: Varrock Coordinates 3211, 3424 represents one tile.''

===Tile Chunk=== A chunk of tiles, 8 x 8 in size. Also known as a region
before the scope of a region was understood. The chunk is considered a
point so it has X and Y coordinates. There are two forms of a Chunk,
formatted and non; a formatted chunks equation is:

int chunkX = (getAbsoluteX() \>\> 3) - 6; int chunkY = (getAbsoluteY()
\>\> 3) - 6;

This centers the chunk on the map, more on that later.

The normal chunk equation is:

int chunkX = (getAbsoluteX() \>\> 3); int chunkY = (getAbsoluteY() \>\>
3);

''Example: The Coordinates \[3211, 3424\] Chunk X (formatted) is 395 and
the Chunk Y (un-formatted) is 428.''

===Region=== A region is 64 x 64 in size, or 8 x 8 in chunks. The region
is considered a point so it has X and Y coordinates. The equation for
finding the region the coordinates is within is:

int regionx = (getUnformattedRegionX() \>\> 3);
//getUnformatedRegionX()/8; int regiony = (getUnformattedRegionY() \>\>
3); //getUnformatedRegionY()/8;

''Example: The Coordinates \[3211, 3424\] Region X is 50 and the Region
Y is 53.''

Note: The Region X and Region Y coordinates are traditionally not used
in server location calculations; but practical region systems should use
this calculation for many purposes.

===Map=== There is no calculation for a map, and there is no Map X or
Map Y. A Map is, however, a 104 x 104 area made up of 13 x 13 chunks.
Why is the number not even you may ask? Because it has a center. The
\[7, 7\] map chunk of the map is the center, and is also the formatted
chunk. When a region update is called by the server, a new map is
called, but you must understand that the formatted chunk never changes;
the tiles in the map, however, are updated and trimmed. When the player
moves out of the formatted chunk, the map is re-positioned to make that
chunk the center yet again. As I said, a new update is not needed every
time the player enters a new region, but when the range of +- 32 from
the point in the center of the chunk is reached, an update is required
to update the map to the new objects so that the 'black space' or fog is
not reached. Confused?

===Diagram=== \[http://i.imgur.com/C3huO.png External Image\]

The active chunk is the chunk in which the player resides. The definite
rendering chunks are the chunks in which will be rendered on the players
screen no matter where they are in the active chunk. The indefinite
rendering chunks are the chunks in which depending on where the player
is within the active chunk they may be rendered or not. Remember this
depends on the +- distance of 32 from the players absolute position. The
queue chunks are pre-loaded chunks in which after the active chunk is
moved may be disposed of or activated depending upon the direction in
which the active chunk changes.

==Loading==

These were the regions loaded for the coordinates \[3183, 3217\]:

\[http://i.imgur.com/ydl78.png External Image\]

If you can imagine a puzzle, a 64 x 64 piece does not fit equally within
the 104 x 104 area. So bits of each region are taken that are within the
104 x 104 map area.

The amount of regions that are to be loaded can be calculated this way:

Please note that Region X and Region Y are not formatted.

int amt = 0; for(int i21 = (player.getLocation().getRegionX() - 6) / 8;
i21 \<= (player.getLocation().getRegionX() + 6) / 8; i21++) { for(int
k23 = (player.getLocation().getRegionY() - 6) / 8; k23 \<=
(player.getLocation().getRegionY() + 6) / 8; k23++) amt++; }

Along with this, the base X and base Y of each of the region can be
calculated:

for(int i21 = (player.getLocation().getRegionX() - 6) / 8; i21 \<=
(player.getLocation().getRegionX() + 6) / 8; i21++) { for(int k23 =
(player.getLocation().getRegionY() - 6) / 8; k23 \<=
(player.getLocation().getRegionY() + 6) / 8; k23++)
System.out.println(i21+\" X "+(i21 \<\< 6)+","+k23+" Y \"+(k23 \<\<
6));;; }

The 'X' and 'Y' coordinates represents the coordinates of the region as
depicted in the diagram. After the regions are loaded they are trimmed
to the tiles that are necessary.

Well hope this gave you some idea of how regions are loaded and such,
tell me if you need explanation on anything.

Heres an example of a location class that I wrote, sorry for the lack of
comments. If you read everything then this should make sense:

package net.forge.content.world.node; /\*\* \* RuneForge \| 317 \*
Location.java \* @version 1.0.0 \* @author SiniSoul (SiniSoul\@live.com)
\*/ public final class Location {

    /**
     * The Tile X and Y coordinates.
     */
    private int tilex = 0, 
                tiley = 0;

    /**
     * The Height of the location.
     */
    private int height = 0;

    /**
     * The asynchronous Chunk X and Y coordinates; used in region updating. 
     */
    private int chunkx = 0,
                chunky = 0;

    /**
     * 
     * @param tilex 
     */
    public void setTileX(int tilex) {
        this.tilex = (tilex & 0xFFFF);
    }

    /**
     * 
     * @return 
     */
    public int getTileX() {
        return tilex;
    }

    /**
     * 
     * @param tilex 
     */
    public void setTileY(int tiley) {
        this.tiley = (tiley & 0xFFFF);
    }

    /**
     * 
     * @return 
     */
    public int getTileY() {
        return tiley;
    }

    /**
     * 
     * @param formated If the chunk is formatted for map positioning or
     *                 other formatted chunk comparison.    
     * @return 
     */
    public int calculateChunkX(boolean formated) {
        return formated ? (getTileX() >> 3) - 6 : (getTileX() >> 3);
    }

    /**
     * 
     * @param formated If the chunk is formatted for map positioning or
     *                 other formatted chunk comparison.                
     * @return 
     */
    public int calculateChunkY(boolean formated) {
        return formated ? (getTileY() >> 3) - 6 : (getTileY() >> 3);
    }

    /**
     * 
     */
    public void updateChunkX() {
        this.chunkx = calculateChunkX(true);
    }

    /**
     * 
     */
    public void updateChunkY() {
        this.chunkx = calculateChunkY(true);
    }

    /**
     * 
     * @return 
     */
    public int getChunkX() {
        return chunkx;
    }

    /**
     * 
     * @return 
     */
    public int getMapLocalX() {
        return getTileX() - (getChunkX() << 3);
    }

    /**
     * 
     * @return 
     */
    public int getChunkY() {
        return chunky;
    }

    /**
     * 
     * @return 
     */
    public int getMapLocalY() {
        return getTileX() - (getChunkY() << 3);
    }

    /**
     * 
     * @param height 
     */
    public void setHeight(int height) {
        this.height = (height & 0x3);
    }

    /**
     * 
     * @return 
     */
    public int getHeight() {
        return height;
    }

    /**
     * 
     * @return 
     */
    public int getRegionX() {
        return calculateChunkX(false) >> 3;
    }

    /**
     * 
     * @return 
     */
    public int getRegionLocalX() {
        return getTileX() - (getRegionX() << 6);
    }

    /**
     * 
     * @return 
     */
    public int getRegionY() {
        return calculateChunkY(false) >> 3;
    }

    /**
     * 
     * @return 
     */
    public int getRegionLocalY() {
        return getTileY() - (getRegionY() << 6);
    }

    /**
     * 
     * @param tilex
     * @param tiley
     * @param height 
     */
    public void set(int tilex, int tiley, int height) {
        setTileX(tilex);
        setTileY(tiley);
        setHeight(height);
    }

    /**
     * 
     * @param tilex
     * @param tiley
     * @param height 
     */
    public Location(int tilex, int tiley, int height) {
        set(tilex, tiley, height);
        updateChunkX();
        updateChunkY();
    }

}
