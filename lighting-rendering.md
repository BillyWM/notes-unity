[Unity lighting clinic 1](https://www.youtube.com/watch?v=JVkv-hU0TmY)
  * 5:00 Mark static to participate in baked GI
  * 7:00 Directional light not set to `baked` will cast through 1-sided geometry
  * 10:00 Generate lightmap UVs. `Select mesh -> Generate lightmap UVs`
  * 12:00 Select `Standard` shader on object for PBR if using a legacy shader
  * 14:00 Ambient occlusion baking: `Lighting` tab -> `Lightmapping` settings -> ambient occlusion
  * 15:00 Mistake: Transparency in albedo channel but just wall behind glass. Increase smoothness too
  * 15:45 Glass reflecting skybox. Need `reflection probe`
