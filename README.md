# UTM Projection Analysis

## 1. UTM Coordinate System

**UTM** (Universal Transverse Mercator Grid System) is a **Plane Rectangular Coordinate System**. This system ignores the elevation information and regards the Earth's surface as an ideal ellipsoid.

## 2. UTM Grid Zones of the World

- **Longitude Zones:** There are 60 longitudinal projection zones numbered **1** to **60** starting at 180°W. Each of these zones is **6 degrees** wide. Region 1 covers the region from 180°W to 174°W, and then the region number increases eastward until Region 60, covering the region from 174°E to 180°E.
- **Latitude Zones:** There are 20 latitudinal zones spanning the latitudes 80°S to 84°N and denoted by the letters **C** to **X**, ommitting the letters I and O. Each of these is **8 degrees** south-north, apart from zone X which is 12 degrees south-north. N is the first north latitude zone, the letters after N belong to the north latitude zones, and the letters before N belong to the south latitude zones. It is worth noting that the polar regions further south at 80°S and further north at 84°N are not included in this system.
- Specific UTM grid zones can refer to the [link](www.dmap.co.uk/utmworld.htm).
- As approaching the boundary of the UTM region, the scale distortion will gradually increase. However, in practice, we often need to measure a series of positions in two adjacent areas, so it is particularly convenient and necessary to use a single grid for measurement. If necessary, we can appropriately extend the measurement results to a certain range of adjacent areas.

## 3. WGS84 and UTM

- **WGS84:** A coordinate system used by the **GPS** (Global Positioning System), which uses longitude and latitude to indicate geographic location. WGS84 is a coordinate system based on the center of the Earth, that is, its origin is the centroid of the Earth.

- **UTM:** This is a system that uses a **2-D Cartesian** coordinate system to represent the geographical location. It divides the Earth's surface into multiple regions (except for the near-Arctic and near-Antarctic regions), each of which uses its own Plane Rectangular Coordinate System. UTM is a surface-based coordinate system, that is, its origin is a point on the surface of the Earth. 

- WGS84 is the spherical coordinates, including latitude and longitude, the unit is **degree**. UTM is a plane coordinate, including x- and y- coordinates, the unit is **meter**.

- **Conversion formula:** $$Longitude\\_Zone = int(\frac{Longitude}{6}) + 31$$

## 4. Tools and Codes

- [epsg.io](https://epsg.io/map#srs=4326&x=117.290039&y=31.952162&z=6&layer=streets)
- `Python` Package [UTM](https://github.com/Turbo87/utm)
