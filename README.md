<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Arch Linux: Flatpak Vinegar Studio Guide</title>
</head>
<body>
    <h1 align="center">
        <img src="https://github.com/Nightro-Fx/Flatpak-Vinegar-Guide/blob/main/img/Flathub.png" width="40" alt="Logo"/> 
        Arch Linux: Flatpak Vinegar Studio Guide
    </h1>

    <h4>❤️ Acknowledgements</h4>
    <p>
        Special thanks to <a href="https://vinegarhq.org/">VinegarHQ</a> for creating the Vinegar launcher.<br/>
        This guide is based on the original by 
        <a href="https://github.com/Nightro-Fx/Flatpak-Vinegar-Guide">Nightro-Fx</a>.<br/>
        Further support is available via the support server: 
        <a href="https://discord.gg/kNHaaFsGZ2">Join Here</a>.
    </p>

    <h5>✅ Installing Roblox Studio via Flatpak on Arch</h5>
    <pre><code>sudo pacman -Syu
sudo pacman -S flatpak gnome-software --needed
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak install flathub org.vinegarhq.Vinegar -y
flatpak run org.vinegarhq.Vinegar
    </code></pre>

    <h5>📦 Adding 3D Model Support (Filesystem Access)</h5>
    <pre><code>flatpak override --user --filesystem=home org.vinegarhq.Vinegar
flatpak override --user --show org.vinegarhq.Vinegar
    </code></pre>

    <blockquote>
        <strong>TIP:</strong> Your <em>drive_c</em> is located at:<br/>
        <code>~/.var/app/org.vinegarhq.Vinegar/data/vinegar/prefixes/studio</code><br/>
        Place models or local assets here if needed.
    </blockquote>

    <h5>⚙️ Configuring Vinegar (Enable Vulkan)</h5>
    <pre><code>[studio]
renderer = "Vulkan"
    </code></pre>

    <p>
        <img src="https://github.com/Nightro-Fx/Flatpak-Vinegar-Guide/blob/main/img/Main%20Menu.png" width="270" alt="Main Menu"/>
        <img src="https://github.com/Nightro-Fx/Flatpak-Vinegar-Guide/blob/main/img/Config%20Menu.png" width="270" alt="Config Menu"/>
        <img src="https://github.com/Nightro-Fx/Flatpak-Vinegar-Guide/blob/main/img/Documentation.png" width="270" alt="Documentation"/>
    </p>

    <blockquote>
        <strong>IMPORTANT:</strong> See the official documentation:<br/>
        <a href="https://vinegarhq.org/Configuration/">Vinegar Configuration Guide</a>
    </blockquote>

    <h5>🚀 Optional: FastFlag Performance Tweaks</h5>
    <pre><code>[studio.fflags]
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
    </code></pre>
</body>
</html>
