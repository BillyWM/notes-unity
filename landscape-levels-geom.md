## Trees, Wind zones
[Custom trees and Unity are not friends (2012)](https://polycount.com/discussion/99121/custom-trees-and-unity-are-not-friends)

> ...but my understanding of how that stuff works is that the the wind zone is just a game object that creates some kind of an offset wave property, and the Unity vegetation just uses shaders that read this property and do vertex animation for the leaves.

> What this means is that (1) you have to be using the Unity nature materials (or a custom shader that's been written to work in the same kind of way), and (2) you need to prepare your meshes for that, based on what the shaders do for their vertex animations. As far as I know, the leaf shaders are written to animate according to vertex position in the UVs. (i.e. the "base" of the leaf or shrub is at v=0, and gets no animation; the "tip" is at v=1 and gets full animation.)

[Custom tree importer](https://assetstore.unity.com/packages/tools/modeling/custom-tree-importer-21079) to assimilate trees into this system

## Probuilder

[Unity at GDC - Rapid worldbuilding with ProBuilder](https://www.youtube.com/watch?v=7k-81UEluyg)

* 
