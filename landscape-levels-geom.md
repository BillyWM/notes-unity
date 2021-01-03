[Fast worldbuilding with Unity's updated Terrain System & ProBuilder - Unite LA](https://www.youtube.com/watch?v=XhYHuju5n6M) (Nov 2018)
  * 11:00 Brush settings -> create neighbor terrains. Sculpt across multiple terrains.
  * 13:45 Tree movement not compatible with URP+HDRP
  * 15:15 `Draw instanced` option. Heightmap, splatmap etc moved to GPU textures and sampled there.

[Terrain tips & tricks | Unity 2019 -Tutorial](https://www.youtube.com/watch?v=bq_PIBWw5oI)
  * 1:15 Move terrain up initially to allow sculpting downards. `Paint height` section in terrain tools then `flatten` whole terrain prior to sculpting
  * 7:00 Mountain sculpting.
    * Constantly move mouse so regions don't get too steep
    * Circle terrain initially. Reduce brush size as it gets steeper. Avoid pyramid shape.
    * 7:45 Define branches.
    * Then sub-branches
  * 8:15 Fog from `dust storm` particles standard asset. White tint, increased size, decreased speed, rotation-over-life-time, increased start lifetime, decreased emission-over-time.


## Trees, Wind zones
[Custom trees and Unity are not friends (2012)](https://polycount.com/discussion/99121/custom-trees-and-unity-are-not-friends)

> ...but my understanding of how that stuff works is that the the wind zone is just a game object that creates some kind of an offset wave property, and the Unity vegetation just uses shaders that read this property and do vertex animation for the leaves.

> What this means is that (1) you have to be using the Unity nature materials (or a custom shader that's been written to work in the same kind of way), and (2) you need to prepare your meshes for that, based on what the shaders do for their vertex animations. As far as I know, the leaf shaders are written to animate according to vertex position in the UVs. (i.e. the "base" of the leaf or shrub is at v=0, and gets no animation; the "tip" is at v=1 and gets full animation.)

[Custom tree importer](https://assetstore.unity.com/packages/tools/modeling/custom-tree-importer-21079) to assimilate trees into this system

## Probuilder

[Unity at GDC - Rapid worldbuilding with ProBuilder](https://www.youtube.com/watch?v=7k-81UEluyg)

* 
