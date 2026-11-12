# A-Light Live Bake Preview: Addon

<p>
  <img alt="Unity 2022.3+" src="https://img.shields.io/badge/Unity-2022.3%2B-222?logo=unity">
  <img alt="Needs A-Light" src="https://img.shields.io/badge/needs-A--Light-ff8a3d">
  <img alt="Free" src="https://img.shields.io/badge/price-free-8a6cff">
</p>

an addon for [A-Light](https://github.com/WestTools/A-Light-Unity-GPU-Lightmapper) that shows you a quick rough bake while you move your lights around, so you dont have to sit through a full bake every time you nudge a light

when youre done hit **Stop Preview** and your real bake comes straight back

## what it does

- bakes a fast low quality version of your lighting
- **auto refresh**: bakes the preview again by itself a moment after you change a light
- 3 quality levels: **Draft** (fastest), **Low** and **Medium** (closest to the real bake)
- can also watch your static objects and materials, not just lights
- your real bake is never touched. the preview goes into its own temporary folder that gets deleted when you stop
- saving the scene while previewing still saves your real bake, not the preview
- starting a real bake stops the preview first, so they never mix

## what you need

- **A-Light**, grab it [here](https://github.com/WestTools/A-Light-Unity-GPU-Lightmapper/releases). without it this addon just does nothing
- **Unity 2022.3 or newer**

## how to install

1. install A-Light first if you havent already
2. grab `A-Light-Addon-LiveBakePreview.unitypackage` from [releases](../../releases)
3. in unity go **Assets › Import Package › Custom Package** and import it
4. open **A-Light › Render Lightmaps** and go to the **Addons** tab

## how to use it

1. in the **Addons** tab hit **Start Preview**
2. move your lights around. with **Auto refresh** on it rebakes after you stop for a sec (you can change how long it waits)
3. hit **Refresh** if you want to update it yourself
4. hit **Stop Preview** when youre done and your real lightmaps come back

| setting | what it does |
|---|---|
| Quality | Draft is fastest, Medium looks closest to the real thing but takes longest |
| Auto refresh | rebakes by itself after you change a light |
| Also watch objects | also rebakes when you move static objects or change materials, not just lights |
| Wait (seconds) | how long it waits after your last change before rebaking (0.2 to 10 seconds) |

## good to know

- its not truly real time. every refresh is a small A-Light bake, so unity freezes for a few seconds while it runs. on big maps use **Draft**
- the preview doesnt bake light probes, so moving objects keep your real probe lighting
- the preview is just for looking. it never ends up in your build
- play mode, closing the scene or reloading scripts stops the preview automatically

## contributing

bug reports with screenshots help the most. PRs are welcome

## disclaimer

this will ALWAYS be a free unity package. if anyone sells it to you, you got scammed. feel free to share it
