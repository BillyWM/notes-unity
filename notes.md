### Compiling from Command Line

* https://stackoverflow.com/questions/45081576/how-can-i-compile-a-unity3d-game-project-from-command-line-into-webgl
* https://docs.unity3d.com/Manual/CommandLineArguments.html


### Update / patching / diffing
* https://forum.unity.com/threads/separate-data-unity3d-for-update.588940/
    * AssetBundles and AddressableAssets
    * [Patching with AssetBundles](https://docs.unity3d.com/Manual/AssetBundles-Patching.html)
    > Unity builds AssetBundles with data ordered in a deterministic manner. This allows applications with custom downloaders to implement differential patching.

### Camera
* Cinemachine third-person camera: https://www.youtube.com/watch?v=537B1kJp9YQ

### General

* Enable preview packages: In project settings
* Navigation hotkeys: https://docs.unity3d.com/Manual/SceneViewNavigation.html


### Caveats
 * Shader Graph requires a Scriptable Render Pipeline (URP or HDRP)
     * SRP used to be LWRP

### Rendering
 * URP breakdown: https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@10.2/manual/universalrp-builtin-feature-comparison.html
 * URP lighting: https://learn.unity.com/tutorial/editing-lighting-in-the-lightweight-render-pipeline

### New UI system
* https://docs.unity3d.com/Packages/com.unity.ui@1.0/api/UnityEngine.UIElements.html
* All descend from "VisualElement"
* Runtime: UIDocument "connects VisualElements to GameObjects" https://docs.unity3d.com/Packages/com.unity.ui@1.0/api/UnityEngine.UIElements.UIDocument.html
    * `var uiDocument = GetComponent<UIDocument>();`
* `.Q<...>(...)` query system. Defined as extension methods `UQueryExtensions`. Used on `VisualElement`

### Mecanim

* https://docs.unity3d.com/Manual/MecanimFAQ.html
