# NativeUnityiOS


Here few points make sure you noted steps by steps

Unity Project : Create unity project or use any exiting but UnityFramework supported only unity 2019.3 or later version. Hope you remove Unity ads framework from unity package manager. set valid bundle Id and signing profile team. uncheck Auto Graphics API , set script IL2CPP. Build platform section select iOS with Xcode version or default, put anywhere.

NOTE : if you wana communication b/w native ios to unity or vise versa then create iOS/plugin and c# script in Unity project C# Script and iOS/plugin . you can change file name, function, parameter and 3d model game object according you.

Embed Unity project : open unity export ios Build in xcode (Unity-iPhone.xcodeproj) and before Run check UnityFramework is there or not? Make Data folder target membership to UnityFramework, iOS/plugin(.mm,.h file) file to UnityFramework as a public (dropdown option). Add few line in Unity-iPhone/MainApp/main.mm file in main function after declare ufw [ufw setDataBundleId: “com.unity3d.framework”];

Export UnityFramework: if everything setup ready then run Unity-iphone on Real Device. if successfully run then you will get auto generated UnityFramework.framework so you can keep or Export in your system.

How to use UnityFramework.framework in native ios App : create or exting iOS native app then Import and drag and drop in your app.
create .swift file for embedded unity put these file code or use this file.

NOTE: three functions are import in embedded unity swift for call unity ShowUnity/HideUnity/sendUnityMessageToGameObject.

6. Final Launch: in native ios you can call UnityEmbeddedSwift.showUnity() in viewDidLoad or launch after button press
@objc func onButtonPressed(_ sender: UIButton) { UnityEmbeddedSwift.showUnity() }


https://kushwaha03.medium.com/integration-unity-project-as-a-library-in-native-ios-app-2746bb3c91b0
