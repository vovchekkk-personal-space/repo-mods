# Empress ShopLoaderAPI v2.1.0
- A developer focused API for R.E.P.O. that simplifies custom shop loading with automatic networking, shop level registration, and BepInEx config integration.

## Changelog

### 2.1.0
* Added Safeguards just in-case.

## Discord
- http://discord.gg/empress

**Developers Only:** This is an **API for loading your custom shops**. You still need to **create your own shop Prefab**. This API handles the loading, networking, and integration for you.

## Features & Configuration
* **Automatic Config Generation:** My API automatically generates a configuration entry for ALL shops that use it. Users can find these under `[Registered Shops]` in the `com.Empress.ShopAPI.cfg` file.
* **Shop Level Registration:** Custom shops are registered as shop level entries so compatible level toggle tools can enable or disable them.
* **Seamless Integration:** My API automatically injects your shop into the `LevelGenerator` and handles the `ResourceCache` for both singleplayer and multiplayer pools.

## Dependencies
* BepInEx is required.
* REPOLib is not required by this API.

---

## For Developers

### Critical Requirement: The Truck, Spawn Points, Screens, and Vehicle Charger
Since version 1.1.0, this API overrides the default Shop Start Room. Because of this, you must follow these rules to prevent the game from crashing:

1. **Use the Module Shop as your Base:** When creating your shop, use the **Module Shop** prefab as your foundation. It contains the working shop interior, extractor components, items ect.
2. **COPY THE CURRENT TRUCK:** The Module Shop prefab does not include a truck by default. You MUST open a current standard Shop Start Room, copy the **Truck parent object**, and paste it into your custom shop prefab.
3. **Why?** The Truck handles the game's **Spawn Points, Truck Screens, vehicle charging station, and critical level logic**. If you do not have the current Truck object in your prefab, the game will find zero spawn points or missing shop systems and can crash.

### Implementation Guide

1. **Add EmpressShopAPI.dll as a reference** in your IDE project.
2. **Add** `[BepInDependency("com.Empress.ShopAPI")]` to your plugin metadata.
3. **Call** `ShopAPI.RegisterShop` in your `Awake` method.

```csharp
using BepInEx;
using UnityEngine;
using Empress_ShopLoaderAPI;
using System.IO;

[BepInPlugin("com.YourName.MyCoolShop", "My Cool Shop", "1.0.0")]
[BepInDependency("com.Empress.ShopAPI")]
public class MyShopPlugin : BaseUnityPlugin
{
    private void Awake()
    {
        string bundlePath = Path.Combine(Path.GetDirectoryName(Info.Location), "my_shop_bundle");
        AssetBundle bundle = AssetBundle.LoadFromFile(bundlePath);

        if (bundle != null)
        {
            GameObject myShopPrefab = bundle.LoadAsset<GameObject>("MyShopPrefabName");

            if (myShopPrefab != null)
            {
                ShopAPI.RegisterShop(myShopPrefab, "YourName/MyCoolShop");
            }
        }
    }
}
```

**Credits**
- Omniscye / Empress
