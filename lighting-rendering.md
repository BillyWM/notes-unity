[Unity lighting clinic 1](https://www.youtube.com/watch?v=JVkv-hU0TmY) (Jan 2018)
  * 2:30 `Window` -> `lighting` -> `settings` to get `Lighting` panel
  * 3:00 Disable realtime GI for baked GI
  * 4:30 Mistake: interior wall reflecting skydome because it's not marked static. 
  * 5:00 Mark static to participate in baked GI
  * 7:00 Directional light not set to `baked` will cast through 1-sided geometry
  * 10:00 Generate lightmap UVs. `Select mesh -> Generate lightmap UVs`
  * 12:00 Select `Standard` shader on object for PBR if using a legacy shader
  * 14:00 Ambient occlusion baking: `Lighting` tab -> `Lightmapping` settings -> ambient occlusion
  * 15:00 Mistake: Transparency in albedo channel but just wall behind glass. Increase smoothness too
  * 15:45 Glass reflecting skybox. Need `reflection probe`
  * 16:15 "Every scene should have at least one reflection probe". All materials are at least somewhat reflective
  * 17:30 Reflection probe contributing to lighting
  * 19:15 `Box projection` mode for reflection probe. Only applies to interior scene with "more or less rectangular shape"
  * 20:00 `Build settings` -> `Player settings`. Use `linear` colorspace for PBR. Defaults to `gamma` instead
  * 20:45 Linear for desktop. Some mobile devices still limited to gamma
  * 22:00 Screen image of PC prop should be on `emissive` channel not `albedo`
  * 23:00 `Final gather` in `lightmapping settings`. More accurate shadow in tiny details. Increased bake time.
  * 27:00 Wall artifacts from change in lightmap resolution. Caused by `lightmap compression`; compression artifacts
  
[7 Ways to Optimize your Unity Project with URP](https://www.youtube.com/watch?v=NFBr21V0zvU)
  * 4:00 Generally, put probes *where there's a shift in lighting*; near *shadowed areas* or where *colors change frequently*
  * 5:30 Bake reflections: Lighting panel -> Generate lighting dropdown -> bake reflection probes
  * 5:45 Turn down cubemap resolution if reflective objects won't be viewed close up (Optimizes memory)
  * 6:15 Occlusion culling; camera defaults to drawing everything in view frustum even if hidden behind walls
    * Mark geometry as `occluder static` or `occludee static`
    * 7:00 Window -> rendering -> `occlusion culling` to bake
  * 7:30 Pipeline settings: Edit -> Project settings -> Quality -> select pipeline asset
  * 8:15 reduce `shadow resolution` and `shadow distance` in these settings for performance
    * 8:30 Possibly disable `depth texture` and `opaque texture` and other features not used
  * Enable `SRP batcher`. Batches **meshes that use compatible shader**
  * 9:00 `Window` -> `analysis` -> `frame debugger`. Breakdown of draw calls. Also breakdown of renderer features.
  * 10:30 `Window` -> `Analysis` -> `Profiler`
    
  [Harnessing Light with URP and the GPU Lightmapper | Unite Now 2020](https://www.youtube.com/watch?v=hMnetI4-dNY) (Jul 2020)
  
  * 6:00 (With 2048 shadow resolution of main light) Implemented by casting 2048x2048 texture on scene then checking for shadows within
  * 7:15 `Additional lights` shadow resolution: possibly lower depending on scene. In sample scene, only cast from spotlight attached to gun
  * 8:00 Shadow distance: increasing loses resolution; spreading the resolution across greater distance. Blurrier and artifacted
  * 8:30 Cascades: Different shadow maps per distance. Can choice *how many cascades* and *breakpoints of cascades*
  * 10:30 `Depth bias` and `normal bias`: Combat shadow artifacting caused by above (high distance + low res)
  * 13:15 Feature matrix for URP:
     * Realtime lighting **and** shadows: `directional` + `spotlights`
     * Realtime *light* only: `point lights`
     * Neither: `area lights`
  * 14:00 Make sure objects are marked `static` **and** lighting is marked `baked`
  * 15:00 TIP: Fixing small emissive light not being captured in map. Placed `baked area lights` in front (without appropriate color). Second for bounce-back light.
  * 16:45 `Lightmap resultion` and `texels per unit`
  * 17:00 Baked lightmap dropdown in scene view to check / debug
  * 17:45 `Scale in lightmap` on per-object basis. Reduce resolution (< 1.0) for distant objects
  * 18:45 Quality of bake based on `direct samples`, `indirect samples`, `environment samples`
    * `evironment lights`: Ray shot ***by texels*** and trying to find sky. **Color is sampled** in each bounce
    * 22:00 `bounces` setting related to above. Plus `russian roulette` setting to help baking times (discarding some ray tests)
  * 22:45 Noisy bakes. `Lightmapping settings` -> `Filtering` -> `Advanced` to hide noise
    * 24:30 `Gaussian` filter "doesn't differentiate between any pixel and geometries". Blurs across pixels and across geometries
    * 25:00 `A-Trous`. Slightly better with touching/intersecting geometry. Tries not to blend texels from different geometries
    * 26:00 `Denoisers`. AI based (???). Compatibility based on graphics card
    * 26:45 Filtering is per `UV chart` (UV 'island')
  * 36:00 Settings affecting realtime performance vs bake time and quality
  * 38:00 (Mixed lighting: `baked indirect` vs `subtractive`)
    * Enable `mixed lighting` on `pipeline asset` then select mode in lighting panel
    * ***Set individual lights to mixed***
  * 45:00 Objects average baked light across 4 closest `light probes`
  * 46:30 "organize them in pyramids" (light probes) near *points of interest*
  * 48:00 Excluding small detailed object (plants) from "recieve global illumination" from lightmap. Light probes instead.
    * 49:15 Contributes to GI (casts shadows) but not light by lightmap GI
  * 50:00 Lighting settings -> Scene -> Light probe visualization
  * 50:45 `Contributors/Receivers` visualization mode (Scene view main dropdown). Debugging GI.
  * 55:00 `Importance` value on reflection probe so it takes precedence
    
  
  
  
  
  
  
  
  
  
