### General

* Enable preview packages: In project settings

### New UI system
* https://docs.unity3d.com/Packages/com.unity.ui@1.0/api/UnityEngine.UIElements.html
* All descend from "VisualElement"
* Runtime: UIDocument "connects VisualElements to GameObjects" https://docs.unity3d.com/Packages/com.unity.ui@1.0/api/UnityEngine.UIElements.UIDocument.html
    * `var uiDocument = GetComponent<UIDocument>();`
* `.Q<...>(...)` query system. Defined as extension methods `UQueryExtensions`. Used on `VisualElement`

### Mecanim

* https://docs.unity3d.com/Manual/MecanimFAQ.html
