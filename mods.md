# Mod Stack Documentation

This document tracks the current SurvivalKendy Fabric mod stack, its purpose, and operational notes.

---

# Core

## Fabric API
File: `fabric-api.jar`  
Purpose: Base dependency for Fabric mods.

## Fabric Language Kotlin
File: `fabric-language-kotlin-1.13.11+kotlin.2.3.21.jar`  
Purpose: Kotlin dependency for mods that require it.

## GlitchCore
File: `GlitchCore-fabric-26.1.2-26.1.2.0.0.jar`  
Purpose: Dependency library for worldgen/gameplay mods.

## Cristel Lib
File: `cristellib-fabric-26.1-3.1.3.jar`  
Purpose: Dependency library.

## Lithostitched
File: `lithostitched-1.7.3-fabric-26.1.jar`  
Purpose: Library/dependency for world generation mods.

---

# Crossplay / Authentication

## Geyser
File: `Geyser-Fabric.jar`  
Purpose: Allows Bedrock players to connect to the Java server.

## Floodgate
File: `Floodgate-Fabric-2.2.6-b63.jar`  
Purpose: Allows Bedrock players to join without Java accounts.  
Important: Preserve `config/floodgate/key.pem`.

## EasyAuth
File: `easyauth-mc26.1-3.4.3-SNAPSHOT.48.jar`  
Purpose: Authentication/login system. ( Since the Server is Cracked )

## SkinRestorer
File: `skinrestorer-2.7.1+26.1-fabric.jar`  
Purpose: Skin support/restoration.  
Notes: Bedrock prefixed names may cause Mojang skin lookup warnings.

---

# Permissions / Admin

## LuckPerms
File: `LuckPerms-Fabric-5.5.42.jar`  
Purpose: Permissions and role management.

---

# Optimization / Monitoring

## Lithium
File: `lithium-fabric-0.24.2+mc26.1.2.jar`  
Purpose: General server optimization.

## FerriteCore
File: `ferritecore-9.0.0-fabric.jar`  
Purpose: Memory optimization.

## Krypton
File: `krypton-0.3.0.jar`  
Purpose: Network stack optimization.

## Noisium
File: `noisium-fabric-2.8.4+mc26.1-pre-2.jar`  
Purpose: World generation/performance optimization.

## PacketFixer
File: `packetfixer-fabric-3.3.5-26.1.2.jar`  
Purpose: Packet/network compatibility fixes.  
Notes: Watch carefully for Bedrock/Geyser packet-related issues.

## Spark
File: `spark-1.10.172-fabric.jar`  
Purpose: Performances monitoring and profiling.

---

# World Generation

## Terralith
File: `Terralith_26.1_v2.6.2_Fabric.jar`  
Purpose: Overworld terrain generation.

## Tectonic
File: `tectonic-3.0.22-fabric-26.1.jar`  
Purpose: Terrain shaping/world generation.

## Incendium
File: `Incendium_26.1_v5.4.12.jar`  
Purpose: Nether world generation.

## Nullscape
File: `Nullscape_26.1_v1.2.19.jar`  
Purpose: End world generation.

## Towns and Towers
File: `t_and_t-fabric-neoforge-1.13.11.jar`  
Purpose: Structure generation.

---

# Gameplay / Utility

## ClickVillagers
File: `ClickVillagers-1.6.5+26.1-fabric.jar`  
Purpose: Villager interaction improvements and trade reset features.

## Veinminer
File: `veinminer-fabric-2.7.1.jar`  
Purpose: Vein mining utility.

## Silk
File: `silk-all-1.11.6.jar`  
Purpose: Silk mod/library functionality.

## AntiXray
File: `antixray-fabric-1.4.16+26.1.jar`  
Purpose: Anti-xray protection.

## Chunky
File: `Chunky-Fabric-1.5.3.jar`  
Purpose: Chunk pregeneration.

---

# Operational Notes

- Keep mod versions aligned with Minecraft/Fabric version.
- Test Bedrock features after packet, item, enchantment, or inventory related mod changes.
- Avoid changing Floodgate username prefix or `key.pem` without migration planning.
- Use Spark before guessing performance issues.
- Remove or isolate outdated mods immediately if console spam or TPS issues appear.