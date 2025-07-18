<body>
    <h1 align="center">
        <img src="https://github.com/Nightro-Fx/Flatpak-Vinegar-Guide/blob/main/img/Flathub.png" width="40" alt="Logo"/> 
        Flatpak Vinegar Studio Guide
    </h1>
</html>

#### ❤️ Acknowledgements  
Thank you [VinegarHQ](https://vinegarhq.org/) for making this guide possible. Further support will be provided over Nightro-Fx's support server, [Here](https://discord.gg/kNHaaFsGZ2).

##### Installing Roblox Studio from Flatpak
```bash
sudo pacman -Syu
sudo pacman -S gnome-software
sudo pacman -S flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub org.vinegarhq.Vinegar
flatpak run org.vinegarhq.Vinegar
```
##### Adding 3D Models to Roblox Studio
```
flatpak override --user --filesystem=home org.vinegarhq.Vinegar
flatpak override --user --show org.vinegarhq.Vinegar
```
>[!TIP]
> By default, Your C-Drive named *drive_c* is located at `~/.var/app/org.vinegarhq.Vinegar/data/vinegar/prefixes/studio`, where you can copy your models to.

##### Configuring Vinegar
<img src="https://github.com/Nightro-Fx/Flatpak-Vinegar-Guide/blob/main/img/Main%20Menu.png" width="270" alt="Logo"/> <img src="https://github.com/Nightro-Fx/Flatpak-Vinegar-Guide/blob/main/img/Config%20Menu.png" width="270" alt="Logo"/> <img src="https://github.com/Nightro-Fx/Flatpak-Vinegar-Guide/blob/main/img/Documentation.png" width="270" alt="Logo"/> 

##### Configuration of Vinegar
```
[studio]
renderer = "Vulkan"
```
>[!IMPORTANT]
> Refer to the Official Vinegar Documentation for Configuration Details:
> [Vinegar Configuration Guide](https://vinegarhq.org/Configuration/)

##### Adding Performance FastFlags To Studio (Optional)
```
[studio.fflags]
DFIntTaskSchedulerTargetFps = 120
FIntRenderShadowIntensity = 0
FIntRenderLocalLightUpdatesMax = 8
FIntRenderLocalLightUpdatesMin = 4
DFIntPerformanceControlTextureQualityBestUtility = -1
FIntFRMMinGrassDistance = 0  
FIntFRMMaxGrassDistance = 0  
FIntRenderGrassDetailStrands = 0  
FIntRenderGrassHeightScaler = 0  
DFIntDebugFRMQualityLevelOverride = 1
FFlagGlobalWindRendering = False  
FFlagGlobalWindActivated = False  
```

##### Credits  
This guide contains a straightforward modification that many users might not know how to perform.  
Special thanks to [Nightro-Fx](https://github.com/Nightro-Fx) for developing the original Debian/Ubuntu version.
