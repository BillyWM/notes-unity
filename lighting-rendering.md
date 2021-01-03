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
  
