
* Launch silently with `-batchmode -nographics`
  * https://docs.unity3d.com/Manual/CommandLineArguments.html
* Separate player build
  * Example script to control build, add menu option: https://docs.unity3d.com/ScriptReference/BuildPipeline.BuildPlayer.html
* Shader errors with `-nographics`
  * https://unity3d.com/unity/alpha/2020.1.0a24
      > Shaders: When running with -nographics, shaders will now treat all of their subshaders as 'not supported.' This means that in -nographics environments, APIs like Shader.isSupported will return false, and also that shaders should consume much less memory because they will no longer keep all the unusable compiled shader code in memory.
* Using `BuildOptions.EnableHeadlessMode` with `-batchmode -nographics` https://forum.unity.com/threads/rendertexture-create-failed-during-nographics.594967/
* Cross-compiling to Linux
    * https://forum.unity.com/threads/cannot-build-for-linux-il2cpp-using-unity-2020-2-0b1-on-win-10.964031/
    >I had more or less the same problem with building for Linux on a Windows machine; Installing "Linux (IL2CPP) Target Support" directly from Unity 2020.2.2's What's New Page fixed it for me.
