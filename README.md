# Sev-Crash
---- Minecraft Crash Report ----

WARNING: coremods are present:
  BNBGamingCore (BNBGamingCore-1.12.2-0.8.0.jar)
  AstralCore (astralsorcery-1.12.2-1.8.10.jar)
  MicdoodlePlugin (MicdoodleCore-1.12.2-4.0.1.177.jar)
  CTMCorePlugin (CTM-MC1.12-0.3.0.15.jar)
  LoadingPlugin (Quark-r1.4-123.jar)
  Do not report to Forge! Remove FoamFixAPI (or replace with FoamFixAPI-Lawful) and try again. (foamfix-0.9.9.1-1.12.2-anarchy.jar)
  CorePlugin (SmoothFont-1.12.2-1.15.jar)
  CoreMod (Aroma1997Core-1.12.2-1.3.0.2.jar)
  FarseekCoreMod (Farseek-1.12-2.3.jar)
  Inventory Tweaks Coremod (InventoryTweaks-1.64-dev.jar)
  ForgelinPlugin (Forgelin-1.6.0.jar)
  IELoadingPlugin (ImmersiveEngineering-core-0.12-82.jar)
  LoadingPlugin (ResourceLoader-MC1.12.1-1.5.3.jar)
  AppleCore (AppleCore-mc1.12.2-3.1.1.jar)
  IvToolkit (IvToolkit-1.3.3-1.12.jar)
  BetterFoliageLoader (BetterFoliage-MC1.12-2.1.10.jar)
  TheBetweenlandsLoadingPlugin (TheBetweenlands-3.3.8-core.jar)
Contact their authors BEFORE contacting forge

// I'm sorry, Dave.

Time: 8/17/18 11:41 PM
Description: Ticking memory connection

java.lang.NullPointerException: Ticking memory connection
	at codechicken.multipart.handler.MultipartSaveLoad$TileNBTContainer.onLoad(MultipartSaveLoad.scala:29)
	at net.minecraft.world.World.func_175700_a(World.java:1918)
	at net.minecraft.world.World.func_147448_a(World.java:1945)
	at net.minecraft.world.chunk.Chunk.func_76631_c(Chunk.java:854)
	at net.minecraftforge.common.chunkio.ChunkIOProvider.syncCallback(ChunkIOProvider.java:105)
	at net.minecraftforge.common.chunkio.ChunkIOExecutor.syncChunkLoad(ChunkIOExecutor.java:94)
	at net.minecraft.world.gen.ChunkProviderServer.loadChunk(ChunkProviderServer.java:118)
	at net.minecraft.world.gen.ChunkProviderServer.func_186028_c(ChunkProviderServer.java:89)
	at net.minecraft.world.gen.ChunkProviderServer.func_186025_d(ChunkProviderServer.java:135)
	at net.minecraft.world.World.func_72964_e(World.java:309)
	at net.minecraft.world.World.func_72838_d(World.java:1207)
	at net.minecraft.world.WorldServer.func_72838_d(WorldServer.java:1058)
	at net.minecraft.server.management.PlayerList.func_72377_c(PlayerList.java:376)
	at net.minecraft.server.management.PlayerList.initializeConnectionToPlayer(PlayerList.java:165)
	at shadows.fastbench.net.HijackedPlayerList.initializeConnectionToPlayer(HijackedPlayerList.java:19)
	at net.minecraftforge.fml.common.network.handshake.NetworkDispatcher.completeServerSideConnection(NetworkDispatcher.java:256)
	at net.minecraftforge.fml.common.network.handshake.NetworkDispatcher.access$100(NetworkDispatcher.java:72)
	at net.minecraftforge.fml.common.network.handshake.NetworkDispatcher$1.func_73660_a(NetworkDispatcher.java:205)
	at net.minecraft.network.NetworkManager.func_74428_b(NetworkManager.java:285)
	at net.minecraft.network.NetworkSystem.func_151269_c(NetworkSystem.java:180)
	at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:790)
	at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:668)
	at net.minecraft.server.integrated.IntegratedServer.func_71217_p(IntegratedServer.java:185)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:526)
	at java.lang.Thread.run(Thread.java:748)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Server thread
Stacktrace:
	at codechicken.multipart.handler.MultipartSaveLoad$TileNBTContainer.onLoad(MultipartSaveLoad.scala:29)
	at net.minecraft.world.World.func_175700_a(World.java:1918)
	at net.minecraft.world.World.func_147448_a(World.java:1945)
	at net.minecraft.world.chunk.Chunk.func_76631_c(Chunk.java:854)
	at net.minecraftforge.common.chunkio.ChunkIOProvider.syncCallback(ChunkIOProvider.java:105)
	at net.minecraftforge.common.chunkio.ChunkIOExecutor.syncChunkLoad(ChunkIOExecutor.java:94)
	at net.minecraft.world.gen.ChunkProviderServer.loadChunk(ChunkProviderServer.java:118)
	at net.minecraft.world.gen.ChunkProviderServer.func_186028_c(ChunkProviderServer.java:89)
	at net.minecraft.world.gen.ChunkProviderServer.func_186025_d(ChunkProviderServer.java:135)
	at net.minecraft.world.World.func_72964_e(World.java:309)
	at net.minecraft.world.World.func_72838_d(World.java:1207)
	at net.minecraft.world.WorldServer.func_72838_d(WorldServer.java:1058)
	at net.minecraft.server.management.PlayerList.func_72377_c(PlayerList.java:376)
	at net.minecraft.server.management.PlayerList.initializeConnectionToPlayer(PlayerList.java:165)
	at shadows.fastbench.net.HijackedPlayerList.initializeConnectionToPlayer(HijackedPlayerList.java:19)
	at net.minecraftforge.fml.common.network.handshake.NetworkDispatcher.completeServerSideConnection(NetworkDispatcher.java:256)
	at net.minecraftforge.fml.common.network.handshake.NetworkDispatcher.access$100(NetworkDispatcher.java:72)
	at net.minecraftforge.fml.common.network.handshake.NetworkDispatcher$1.func_73660_a(NetworkDispatcher.java:205)
	at net.minecraft.network.NetworkManager.func_74428_b(NetworkManager.java:285)

-- Ticking connection --
Details:
	Connection: net.minecraft.network.NetworkManager@5aba3030
Stacktrace:
	at net.minecraft.network.NetworkSystem.func_151269_c(NetworkSystem.java:180)
	at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:790)
	at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:668)
	at net.minecraft.server.integrated.IntegratedServer.func_71217_p(IntegratedServer.java:185)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:526)
	at java.lang.Thread.run(Thread.java:748)

-- System Details --
Details:
	Minecraft Version: 1.12.2
	Operating System: Mac OS X (x86_64) version 10.13.4
	Java Version: 1.8.0_181, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 1691314832 bytes (1612 MB) / 4225236992 bytes (4029 MB) up to 4225236992 bytes (4029 MB)
	JVM Flags: 7 total; -XX:-OmitStackTraceInFastThrow -Xms256M -Xmx4096M -XX:MetaspaceSize=256M -XX:+UseConcMarkSweepGC -XX:+CMSIncrementalMode -XX:-UseAdaptiveSizePolicy
	IntCache: cache: 1, tcache: 1, allocated: 6, tallocated: 111
	FML: MCP 9.42 Powered by Forge 14.23.4.2707 263 mods loaded, 263 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored

	| State     | ID                       | Version                      | Source                                            | Signature                                |
	|:--------- |:------------------------ |:---------------------------- |:------------------------------------------------- |:---------------------------------------- |
	| UCHIJAAAA | minecraft                | 1.12.2                       | minecraft.jar                                     | None                                     |
	| UCHIJAAAA | mcp                      | 9.42                         | minecraft.jar                                     | None                                     |
	| UCHIJAAAA | FML                      | 8.0.99.99                    | forge-1.12.2-14.23.4.2707-universal.jar           | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| UCHIJAAAA | forge                    | 14.23.4.2707                 | forge-1.12.2-14.23.4.2707-universal.jar           | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| UCHIJAAAA | ivtoolkit                | 1.3.3-1.12                   | minecraft.jar                                     | None                                     |
	| UCHIJAAAA | micdoodlecore            |                              | minecraft.jar                                     | None                                     |
	| UCHIJAAAA | smoothfontcore           | 1.12.2-1.14                  | minecraft.jar                                     | None                                     |
	| UCHIJAAAA | bnbgamingcore            | 0.8.0                        | minecraft.jar                                     | None                                     |
	| UCHIJAAAA | foamfixcore              | 7.7.4                        | minecraft.jar                                     | None                                     |
	| UCHIJAAAA | smoothfont               | 1.12.2-1.15                  | SmoothFont-1.12.2-1.15.jar                        | None                                     |
	| UCHIJAAAA | movillages               | 1.5.4                        | [1.12]MoVillages-1.5.4.jar                        | None                                     |
	| UCHIJAAAA | gobblecore               | 1.12-0.1.6.35                | GobbleCore-1.12-0.1.6.35.jar                      | None                                     |
	| UCHIJAAAA | charcoalblock            | 1.1                          | A Block of Charcoal-1.1.jar                       | None                                     |
	| UCHIJAAAA | advancedmortars          | 1.12.2-1.6.21                | advancedmortars-1.12.2-1.6.21.jar                 | None                                     |
	| UCHIJAAAA | crafttweaker             | 4.1.8                        | CraftTweaker2-1.12-4.1.8.jar                      | None                                     |
	| UCHIJAAAA | mtlib                    | 3.0.4                        | MTLib-3.0.4.jar                                   | None                                     |
	| UCHIJAAAA | modtweaker               | 4.0.12                       | modtweaker-4.0.12.jar                             | None                                     |
	| UCHIJAAAA | jei                      | 4.9.2.196                    | jei_1.12.2-4.9.2.196.jar                          | None                                     |
	| UCHIJAAAA | abyssalcraft             | 1.9.4.9                      | AbyssalCraft-1.12.2-1.9.4.9.jar                   | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
	| UCHIJAAAA | ctm                      | MC1.12-0.3.0.15              | CTM-MC1.12-0.3.0.15.jar                           | None                                     |
	| UCHIJAAAA | chisel                   | MC1.12.2-0.2.0.31            | Chisel-MC1.12.2-0.2.0.31.jar                      | None                                     |
	| UCHIJAAAA | mantle                   | 1.12-1.3.2.24                | Mantle-1.12-1.3.2.24.jar                          | None                                     |
	| UCHIJAAAA | tconstruct               | 1.12.2-2.10.1.84             | TConstruct-1.12.2-2.10.1.84.jar                   | None                                     |
	| UCHIJAAAA | acintegration            | 1.6.2                        | AbyssalCraft Integration-1.12.2-1.6.2.jar         | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
	| UCHIJAAAA | fastbench                | 1.5.0                        | FastWorkbench-1.12.2-1.5.0.jar                    | None                                     |
	| UCHIJAAAA | actuallyadditions        | 1.12.2-r135                  | ActuallyAdditions-1.12.2-r135.jar                 | None                                     |
	| UCHIJAAAA | baubles                  | 1.5.2                        | Baubles-1.12-1.5.2.jar                            | None                                     |
	| UCHIJAAAA | actuallybaubles          | 1.1                          | ActuallyBaubles-1.12-1.1.jar                      | None                                     |
	| UCHIJAAAA | animalium                | 0.3.7                        | Animalium-0.3.7.jar                               | None                                     |
	| UCHIJAAAA | antiqueatlas             | 4.4.9                        | antiqueatlas-1.12.2-4.4.9.jar                     | None                                     |
	| UCHIJAAAA | antiqueatlasoverlay      | 1.2                          | antiqueatlas-1.12.2-4.4.9.jar                     | None                                     |
	| UCHIJAAAA | examplemod               | 1.0                          | antiqueatlas-1.12.2-4.4.9.jar                     | None                                     |
	| UCHIJAAAA | applecore                | 3.1.1                        | AppleCore-mc1.12.2-3.1.1.jar                      | None                                     |
	| UCHIJAAAA | immersiveengineering     | 0.12-82                      | ImmersiveEngineering-0.12-82.jar                  | 4cb49fcde3b43048c9889e0a3d083225da926334 |
	| UCHIJAAAA | geolosys                 | 1.9.3                        | Geolosys-1.12.2-1.9.3.jar                         | None                                     |
	| UCHIJAAAA | redstoneflux             | 2.0.2                        | RedstoneFlux-1.12-2.0.2.3-universal.jar           | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | mekanism                 | 1.12.2-9.4.11.346            | Mekanism-1.12.2-9.4.11.346.jar                    | None                                     |
	| UCHIJAAAA | natura                   | 1.12.2-4.3.2.49              | natura-1.12.2-4.3.2.49.jar                        | None                                     |
	| UCHIJAAAA | betterwithmods           | ${version}                   | BetterWithMods-1.12-2.1.24.jar                    | None                                     |
	| UCHIJAAAA | appleskin                | 1.0.9                        | AppleSkin-mc1.12-1.0.9.jar                        | None                                     |
	| UCHIJAAAA | appliedenergistics2      | rv5-stable-11                | appliedenergistics2-rv5-stable-11.jar             | None                                     |
	| UCHIJAAAA | armoreablemobs           | 1.1.2                        | armoreablemobs-1.12-1.1.6-4.jar                   | None                                     |
	| UCHIJAAAA | aroma1997core            | 1.3.0.2                      | Aroma1997Core-1.12.2-1.3.0.2.jar                  | dfbfe4c473253d8c5652417689848f650b2cbe32 |
	| UCHIJAAAA | aromabackup              | 2.1.1.3                      | AromaBackup-1.12.2-2.1.1.3.jar                    | dfbfe4c473253d8c5652417689848f650b2cbe32 |
	| UCHIJAAAA | aromabackuprecovery      | 2.1.1.3                      | AromaBackup-1.12.2-2.1.1.3.jar                    | None                                     |
	| UCHIJAAAA | astikoor                 | 1.1.0                        | astikoor_horse-carts-1.1.0a.jar                   | None                                     |
	| UCHIJAAAA | astralsorcery            | 1.8.10                       | astralsorcery-1.12.2-1.8.10.jar                   | a0f0b759d895c15ceb3e3bcb5f3c2db7c582edf0 |
	| UCHIJAAAA | quark                    | r1.4-123                     | Quark-r1.4-123.jar                                | None                                     |
	| UCHIJAAAA | autoreglib               | 1.3-17                       | AutoRegLib-1.3-17.jar                             | None                                     |
	| UCHIJAAAA | base                     | 3.7.2                        | base-1.12.2-3.7.2.jar                             | None                                     |
	| UCHIJAAAA | bdlib                    | 1.14.3.12                    | bdlib-1.14.3.12-mc1.12.2.jar                      | None                                     |
	| UCHIJAAAA | bedrockbgone             | 5.0.8                        | BedrockBGone-1.12.2-5.0-b8.jar                    | None                                     |
	| UCHIJAAAA | betterwithaddons         | @VERSION@                    | Better With Addons-0.41.jar                       | None                                     |
	| UCHIJAAAA | betteradvancements       | 0.0.7.42                     | BetterAdvancements-1.12.2-0.0.7.42.jar            | None                                     |
	| UCHIJAAAA | betterbuilderswands      | 0.11.1                       | BetterBuildersWands-1.12-0.11.1.24569d0d70.jar    | None                                     |
	| UCHIJAAAA | betterfoliage            | 2.1.10                       | BetterFoliage-MC1.12-2.1.10.jar                   | None                                     |
	| UCHIJAAAA | bibliocraft              | 2.4.4                        | BiblioCraft[v2.4.4][MC1.12.2].jar                 | None                                     |
	| UCHIJAAAA | cyclicmagic              | 1.15.8                       | Cyclic-1.12.2-1.15.8.jar                          | None                                     |
	| UCHIJAAAA | waila                    | 1.8.26                       | Hwyla-1.8.26-B41_1.12.2.jar                       | None                                     |
	| UCHIJAAAA | modularrouters           | 1.12.2-3.1.5                 | modular-routers-1.12.2-3.1.5.jar                  | None                                     |
	| UCHIJAAAA | guideapi                 | 1.12-2.1.5-60                | Guide-API-1.12-2.1.5-60.jar                       | None                                     |
	| UCHIJAAAA | bloodmagic               | 1.12.2-2.2.12-97             | BloodMagic-1.12.2-2.2.12-97.jar                   | None                                     |
	| UCHIJAAAA | bnbgaminglib             | 2.11.2                       | BNBGamingLib-1.12-2.11.2.jar                      | None                                     |
	| UCHIJAAAA | bonsaitrees              | 1.0.5                        | bonsaitrees-1.0.5-b77.jar                         | None                                     |
	| UCHIJAAAA | bookshelf                | 2.3.544                      | Bookshelf-1.12.2-2.3.544.jar                      | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | buildcraftlib            | 7.99.17                      | buildcraft-core-7.99.17.jar                       | None                                     |
	| UCHIJAAAA | buildcraftcore           | 7.99.17                      | buildcraft-core-7.99.17.jar                       | None                                     |
	| UCHIJAAAA | buildcraftbuilders       | 7.99.17                      | buildcraft-builders-7.99.17.jar                   | None                                     |
	| UCHIJAAAA | buildcraftfactory        | 7.99.17                      | buildcraft-factory-7.99.17.jar                    | None                                     |
	| UCHIJAAAA | buildcraftrobotics       | 7.99.17                      | buildcraft-robotics-7.99.17.jar                   | None                                     |
	| UCHIJAAAA | buildcrafttransport      | 7.99.17                      | buildcraft-transport-7.99.17.jar                  | None                                     |
	| UCHIJAAAA | buildcraftsilicon        | 7.99.17                      | buildcraft-silicon-7.99.17.jar                    | None                                     |
	| UCHIJAAAA | caliper                  | 1.1.35                       | Caliper-1.12.2-1.1.35.jar                         | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | car                      | 1.2.11                       | car-1.2.11.jar                                    | None                                     |
	| UCHIJAAAA | gamestages               | 1.0.86                       | GameStages-1.12.2-1.0.86.jar                      | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | carryon                  | 1.9                          | CarryOn MC1.12.2 v1.9.jar                         | None                                     |
	| UCHIJAAAA | cd4017be_lib             | 6.2.4                        | CD4017BE_lib-1.12.2-6.2.4.jar                     | None                                     |
	| UCHIJAAAA | ceramics                 | 1.12-1.3.4                   | Ceramics-1.12-1.3.4.jar                           | None                                     |
	| UCHIJAAAA | chameleon                | 1.12-4.1.3                   | Chameleon-1.12-4.1.3.jar                          | None                                     |
	| UCHIJAAAA | chargers                 | 1.0.0                        | Chargers-1.12.2-1.0.0.1.jar                       | 58e787c8aafad8b327883f94d4fa544f936d7b01 |
	| UCHIJAAAA | chiselsandbits           | 14.17                        | chiselsandbits-14.17.jar                          | None                                     |
	| UCHIJAAAA | clienttweaks             | 3.1.8                        | ClientTweaks_1.12.2-3.1.8.jar                     | None                                     |
	| UCHIJAAAA | clumps                   | 2.0.0                        | Clumps-3.0.0.jar                                  | None                                     |
	| UCHIJAAAA | codechickenlib           | 3.1.8.341                    | CodeChickenLib-1.12.2-3.1.8.341-universal.jar     | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| UCHIJAAAA | colouredtooltips         | 1.0.4                        | ColouredTooltips-1.12.2-1.0.4.jar                 | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | cyclopscore              | 0.11.6                       | CyclopsCore-1.12.2-0.11.6.jar                     | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
	| UCHIJAAAA | commoncapabilities       | 1.4.0                        | CommonCapabilities-1.12-1.4.0.jar                 | None                                     |
	| UCHIJAAAA | storagedrawers           | 1.12-5.3.5                   | StorageDrawers-1.12.2-5.3.6.jar                   | None                                     |
	| UCHIJAAAA | refinedstorage           | 1.5.34                       | refinedstorage-1.5.34.jar                         | 57893d5b90a7336e8c63fe1c1e1ce472c3d59578 |
	| UCHIJAAAA | compactmachines3         | 3.0.12                       | compactmachines3-1.12.2-3.0.12-b215.jar           | None                                     |
	| UCHIJAAAA | conarm                   | 0.0.21-rc1                   | conarm-1.12.2-0.0.21-rc1.jar                      | 5d5b8aee896a4f5ea3f3114784742662a67ad32f |
	| UCHIJAAAA | contenttweaker           | 1.12.2-4.5.0                 | ContentTweaker-1.12.2-4.5.0.jar                   | None                                     |
	| UCHIJAAAA | controlling              | 3.0.6                        | Controlling-3.0.6.jar                             | None                                     |
	| UCHIJAAAA | cookingforblockheads     | 6.3.26                       | CookingForBlockheads_1.12.2-6.3.26.jar            | None                                     |
	| UCHIJAAAA | craftstudioapi           | 1.0.0                        | CraftStudio-1.0.0.93-mc1.12-alpha.jar             | None                                     |
	| UCHIJAAAA | ctgui                    | 1.0.0                        | CraftTweaker2-1.12-4.1.8.jar                      | None                                     |
	| UCHIJAAAA | crafttweakerjei          | 2.0.2                        | CraftTweaker2-1.12-4.1.8.jar                      | None                                     |
	| UCHIJAAAA | cucumber                 | 1.1.0                        | cucumber-1.12-1.1.0.jar                           | None                                     |
	| UCHIJAAAA | custommainmenu           | 2.0.8                        | CustomMainMenu-MC1.12.2-2.0.8.jar                 | None                                     |
	| UCHIJAAAA | darkutils                | 1.8.210                      | DarkUtils-1.12.2-1.8.210.jar                      | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | death_compass            | 0.0.3                        | DeathCompass-0.0.3.jar                            | None                                     |
	| UCHIJAAAA | journeymap               | 1.12.2-5.5.2                 | journeymap-1.12.2-5.5.2.jar                       | None                                     |
	| UCHIJAAAA | defaultoptions           | 9.2.7                        | DefaultOptions_1.12.2-9.2.7.jar                   | None                                     |
	| UCHIJAAAA | despawningspawners       | 1.1                          | despawningspawners-1.1.jar                        | None                                     |
	| UCHIJAAAA | dimensionalcontrol       | 2.10.2                       | DimensionalControl-1.12.2-2.10.2.jar              | None                                     |
	| UCHIJAAAA | dimstages                | 1.0.18                       | DimensionStages-1.12.2-1.0.18.jar                 | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | dungpipe                 | 1.0                          | Dung Pipe-1.2.jar                                 | None                                     |
	| UCHIJAAAA | elevatorid               | 1.3.6                        | ElevatorMod-1.12.2-1.3.6.jar                      | None                                     |
	| UCHIJAAAA | emberroot                | 1.3.7                        | EmberRootZoo-1.12-1.3.7.jar                       | None                                     |
	| UCHIJAAAA | enchdesc                 | 1.1.8                        | EnchantmentDescriptions-1.12.2-1.1.8.jar          | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | enderstorage             | 2.4.3.130                    | EnderStorage-1.12.2-2.4.3.130-universal.jar       | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| UCHIJAAAA | enderutilities           | 0.7.8                        | enderutilities-1.12.2-0.7.8.jar                   | 2b03e1423915a189b8094816baa18f239d576dff |
	| UCHIJAAAA | valkyrielib              | 1.12.2-2.0.11a               | valkyrielib-1.12.2-2.0.11a.jar                    | None                                     |
	| UCHIJAAAA | environmentaltech        | 1.12.2-2.0.11a               | environmentaltech-1.12.2-2.0.11a.jar              | None                                     |
	| UCHIJAAAA | extendedcrafting         | 1.3.7                        | extendedcrafting-1.12-1.3.7.jar                   | None                                     |
	| UCHIJAAAA | galacticraftcore         | 4.0.1.177                    | GalacticraftCore-1.12.2-4.0.1.177.jar             | None                                     |
	| UCHIJAAAA | galacticraftplanets      | 4.0.1.177                    | Galacticraft-Planets-1.12.2-4.0.1.177.jar         | None                                     |
	| UCHIJAAAA | mjrlegendslib            | 1.12.2-1.1.4                 | MJRLegendsLib-1.12.2-1.1.4.jar                    | b02331787272ec3515ebe63ecdeea0d746653468 |
	| UCHIJAAAA | extraplanets             | 1.12.2-0.3.8                 | ExtraPlanets-1.12.2-0.3.8.jar                     | b02331787272ec3515ebe63ecdeea0d746653468 |
	| UCHIJAAAA | fbp                      | 2.4.0                        | FancyBlockParticles-1.12.x-2.4.0.jar              | None                                     |
	| UCHIJAAAA | farmingforblockheads     | 3.1.17                       | FarmingForBlockheads_1.12.2-3.1.17.jar            | None                                     |
	| UCHIJAAAA | farseek                  | 2.3                          | Farseek-1.12-2.3.jar                              | None                                     |
	| UCHIJAAAA | fat_cat                  | 0.0.5                        | FatCat-0.0.5.jar                                  | None                                     |
	| UCHIJAAAA | ferdinandsflowers        | 1.10.1b                      | Ferdinands Flowers-1.10.1b-1.12.jar               | None                                     |
	| UCHIJAAAA | findme                   | 1.0                          | findme-1.12.2-1.0.1-5.jar                         | None                                     |
	| UCHIJAAAA | foamfix                  | 0.9.9.1-1.12.2               | foamfix-0.9.9.1-1.12.2-anarchy.jar                | None                                     |
	| UCHIJAAAA | forgelin                 | 1.6.0                        | Forgelin-1.6.0.jar                                | None                                     |
	| UCHIJAAAA | forgemultipartcbe        | 2.4.2.58                     | ForgeMultipart-1.12.2-2.4.2.58-universal.jar      | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| UCHIJAAAA | microblockcbe            | 2.4.2.58                     | ForgeMultipart-1.12.2-2.4.2.58-universal.jar      | None                                     |
	| UCHIJAAAA | minecraftmultipartcbe    | 2.4.2.58                     | ForgeMultipart-1.12.2-2.4.2.58-universal.jar      | None                                     |
	| UCHIJAAAA | galacticrafttweaker      | 1.12.2-1.0.1                 | GalacticraftTweaker-1.12.2-1.0.1.jar              | b02331787272ec3515ebe63ecdeea0d746653468 |
	| UCHIJAAAA | advgenerators            | 0.9.20.12                    | generators-0.9.20.12-mc1.12.2.jar                 | None                                     |
	| UCHIJAAAA | harvest                  | 1.12-1.2.6-18                | Harvest-1.12-1.2.6-18.jar                         | None                                     |
	| UCHIJAAAA | horsepower               | 2.6.1                        | HorsePower-1.12.2-2.6.1.64.jar                    | cd7e958342770a8b17c919055da42c24dfefd879 |
	| UCHIJAAAA | huntingdim               | 1.0.24                       | HuntingDimension-1.12.2-1.0.24.jar                | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | mcjtylib_ng              | 2.6.7                        | mcjtylib-1.12-2.6.7.jar                           | None                                     |
	| UCHIJAAAA | immcraft                 | 1.4.1                        | immcraft-1.12-1.4.1.jar                           | None                                     |
	| UCHIJAAAA | immersivepetroleum       | 1.1.9                        | immersivepetroleum-1.12.2-1.1.9.jar               | None                                     |
	| UCHIJAAAA | immersivetech            | 1.3.10                       | immersivetech-1.12-1.3.10.jar                     | None                                     |
	| UCHIJAAAA | improvedbackpacks        | 1.12.2-1.2.0.3               | ImprovedBackpacks-1.12.2-1.2.0.3.jar              | None                                     |
	| UCHIJAAAA | incontrol                | 3.8.0                        | incontrol-1.12-3.8.0.jar                          | None                                     |
	| UCHIJAAAA | indlog                   | 1.2.3                        | InductiveLogistics-1.12.2-1.2.3.jar               | None                                     |
	| UCHIJAAAA | teslacorelib             | 1.0.14                       | tesla-core-lib-1.12.2-1.0.14.jar                  | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | industrialforegoing      | 1.12.2-1.12.2                | industrialforegoing-1.12.2-1.10.0-173.jar         | None                                     |
	| UCHIJAAAA | infoaccessories          | 1.0.6                        | InfoAccessories-1.12.2-1.0.6.jar                  | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | integrateddynamics       | 0.11.12                      | IntegratedDynamics-1.12.2-0.11.12.jar             | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
	| UCHIJAAAA | integrateddynamicscompat | 1.0.0                        | IntegratedDynamics-1.12.2-0.11.12.jar             | None                                     |
	| UCHIJAAAA | inventorytweaks          | 1.64-dev+release.110.b4fac73 | InventoryTweaks-1.64-dev.jar                      | 55d2cd4f5f0961410bf7b91ef6c6bf00a766dcbe |
	| UCHIJAAAA | ironbackpacks            | 1.12.2-3.0.8-12              | IronBackpacks-1.12.2-3.0.8-12.jar                 | None                                     |
	| UCHIJAAAA | ironchest                | 1.12.2-7.0.40.824            | ironchest-1.12.2-7.0.40.824.jar                   | None                                     |
	| UCHIJAAAA | ironjetpacks             | 1.0.5                        | ironjetpacks-1.12-1.0.5.jar                       | None                                     |
	| UCHIJAAAA | itemstages               | 1.0.33                       | ItemStages-1.12.2-1.0.33.jar                      | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | jmapstages               | @VERSION@                    | JourneyMapStages-1.12.2-1.0.3.jar                 | None                                     |
	| UCHIJAAAA | jarm                     | 1.1.2                        | Just A Raft Mod-1.1.2.jar                         | None                                     |
	| UCHIJAAAA | jaff                     | 1.7_for_1.12                 | JustAFewFish-1.7_for_1.12.jar                     | None                                     |
	| UCHIJAAAA | justenoughpetroleum      | 0.1                          | JustEnoughPetroleum-0.1.jar                       | None                                     |
	| UCHIJAAAA | kleeslabs                | 5.4.10                       | KleeSlabs_1.12.2-5.4.10.jar                       | None                                     |
	| UCHIJAAAA | lttweaker                | 1.1.14                       | LootTableTweaker-1.12.2-1.1.14.jar                | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | magma_monsters           | 0.3.0                        | MagmaMonsters-0.3.0.jar                           | None                                     |
	| UCHIJAAAA | mercurius                | 1.0.6                        | Mercurius-1.12.2.jar                              | None                                     |
	| UCHIJAAAA | mobends                  | 0.24                         | mobends-0.24_for_MC-1.12.jar                      | None                                     |
	| UCHIJAAAA | mob_grinding_utils       | 0.3.6                        | MobGrindingUtils-0.3.6.jar                        | None                                     |
	| UCHIJAAAA | mobstages                | 1.0.7                        | MobStages-1.12.2-1.0.7.jar                        | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | modularmachinery         | 1.9.4                        | modularmachinery-1.9.4.jar                        | None                                     |
	| UCHIJAAAA | morpheus                 | 1.12-3.3.2                   | Morpheus-1.12-3.3.2.jar                           | None                                     |
	| UCHIJAAAA | mousetweaks              | 2.8                          | MouseTweaks-2.8-mc1.12.1.jar                      | None                                     |
	| UCHIJAAAA | mputils                  | 1.5.6                        | MPUtils-1.12.2-1.5.6.jar                          | None                                     |
	| UCHIJAAAA | mpbasic                  | 1.4.7                        | mpbasic-1.12.2-1.4.8.jar                          | None                                     |
	| UCHIJAAAA | multiblockstages         | 1.0-SNAPSHOT                 | multiblockstages-1.0.1.jar                        | None                                     |
	| UCHIJAAAA | mundaneredstone          | 1.1.3                        | MundaneRedstone-1.1.3.jar                         | None                                     |
	| UCHIJAAAA | mysticalagriculture      | 1.6.10                       | mysticalagriculture-1.12-1.6.10.jar               | None                                     |
	| UCHIJAAAA | mysticalagradditions     | 1.2.8                        | mysticalagradditions-1.12-1.2.8.jar               | None                                     |
	| UCHIJAAAA | mystagradcompat          | 1.2                          | mystagradcompat-1.2.jar                           | None                                     |
	| UCHIJAAAA | naturescompass           | 1.5.1                        | NaturesCompass-1.12.2-1.5.1.jar                   | None                                     |
	| UCHIJAAAA | neat                     | 1.4-15                       | Neat 1.4-15.jar                                   | None                                     |
	| UCHIJAAAA | nex                      | 2.1.14.15                    | NetherEx-1.12-2.1.14.15.jar                       | None                                     |
	| UCHIJAAAA | norecipebook             | 1.2.1                        | noRecipeBook_v1.2.2formc1.12.2.jar                | None                                     |
	| UCHIJAAAA | nei                      | 2.4.1                        | NotEnoughItems-1.12.2-2.4.1.233-universal.jar     | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| UCHIJAAAA | noworldgen5you           | 1.0.6                        | NoWorldgen5You-1.12.2-1.0.6.jar                   | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | nutrition                | 3.4.0                        | Nutrition-1.12.2-3.4.0.jar                        | None                                     |
	| UCHIJAAAA | samsocean                | 1.0.1                        | OceanFloor-1.12-1.0.1.jar                         | None                                     |
	| UCHIJAAAA | oreexcavation            | 1.4.118                      | OreExcavation-1.4.118.jar                         | None                                     |
	| UCHIJAAAA | oeintegration            | 2.3.3                        | oeintegration-2.3.3.jar                           | None                                     |
	| UCHIJAAAA | orestages                | 1.0.26                       | OreStages-1.12.2-1.0.26.jar                       | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | overloaded               | 0.0.52                       | Overloaded-1.12.2-0.0.52.jar                      | 644f38521a349310a5dae0239577dc7beebefaec |
	| UCHIJAAAA | pickletweaks             | 2.0.16                       | pickletweaks-1.12-2.0.16.jar                      | None                                     |
	| UCHIJAAAA | placebo                  | 1.3.4                        | Placebo-1.12.2-1.3.4.jar                          | None                                     |
	| UCHIJAAAA | playerskins              | 1.0.4                        | playerskin-1.12.2-1.0.5.jar                       | None                                     |
	| UCHIJAAAA | pneumaticcraft           | 1.12.2-0.6.6-192             | pneumaticcraft-repressurized-1.12.2-0.6.6-192.jar | None                                     |
	| UCHIJAAAA | poweradapters            | 1.0.9                        | PowerAdapters-1.12.2-1.0.9.jar                    | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | prestige                 | 1.0.15                       | Prestige-1.12.2-1.0.15.jar                        | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | primalchests             | 1.0.3                        | PrimalChests-1.0.3.jar                            | None                                     |
	| UCHIJAAAA | rustic                   | 1.0.5                        | rustic-1.0.5.jar                                  | None                                     |
	| UCHIJAAAA | thebetweenlands          | 3.3.8                        | TheBetweenlands-3.3.8-universal.jar               | 38067d6878811efb38b6a045521cfd80b9b60b38 |
	| UCHIJAAAA | traverse                 | 1.5.3                        | Traverse-1.12.2-1.5.3-58.jar                      | None                                     |
	| UCHIJAAAA | primal                   | 0.6.56                       | PrimalCore-1.12.2-0.6.56.jar                      | 67a0e286dc0d4b502f3c92ac20b953517b52d0a9 |
	| UCHIJAAAA | progressiontweaks        | 1.12.2-0.3.40                | ProgressionTweaks-1.12.2-0.3.40.jar               | None                                     |
	| UCHIJAAAA | prospectors              | 1.0.1                        | prospectors-1.0.1.jar                             | None                                     |
	| UCHIJAAAA | reborncore               | 3.8.7.295                    | RebornCore-1.12.2-3.8.7.295-universal.jar         | 8727a3141c8ec7f173b87aa78b9b9807867c4e6b |
	| UCHIJAAAA | quantumstorage           | 4.5.0                        | QuantumStorage-1.12-4.5.0.jar                     | None                                     |
	| UCHIJAAAA | quickleafdecay           | 1.2.4                        | QuickLeafDecay-MC1.12.1-1.2.4.jar                 | None                                     |
	| UCHIJAAAA | rangedpumps              | 0.5                          | rangedpumps-0.5.jar                               | None                                     |
	| UCHIJAAAA | realdrops                | 1.2.12                       | RealisticItemDrops-1.2.12.jar                     | None                                     |
	| UCHIJAAAA | rebornstorage            | 1.0.0                        | RebornStorage-1.12.2-3.1.0.50.jar                 | None                                     |
	| UCHIJAAAA | recipestages             | 1.0.8                        | RecipeStages-1.0.8.jar                            | None                                     |
	| UCHIJAAAA | reccomplex               | 1.4.7                        | RecurrentComplex-1.4.7.jar                        | None                                     |
	| UCHIJAAAA | refinedstorageaddons     | 0.3                          | refinedstorageaddons-0.3.jar                      | None                                     |
	| UCHIJAAAA | resourceloader           | 1.5.3                        | ResourceLoader-MC1.12.1-1.5.3.jar                 | d72e0dd57935b3e9476212aea0c0df352dd76291 |
	| UCHIJAAAA | rftools                  | 7.33                         | rftools-1.12-7.33.jar                             | None                                     |
	| UCHIJAAAA | rftoolscontrol           | 1.8.1                        | rftoolsctrl-1.12-1.8.1.jar                        | None                                     |
	| UCHIJAAAA | roadrunner               | 1.0.1                        | roadrunner-1.0.1.jar                              | None                                     |
	| UCHIJAAAA | scannable                | 1.6.3.19                     | Scannable-MC1.12-1.6.3.19.jar                     | None                                     |
	| UCHIJAAAA | sevtweaks                | 0.1.0-null                   | sevtweaks-0.1.0.jar                               | None                                     |
	| UCHIJAAAA | sev_tweaks_npc           | 0.0.4                        | SevTweaksNPC-0.0.4.jar                            | None                                     |
	| UCHIJAAAA | simpleautorun            | 1.12.1-1.2                   | simpleautorun-1.12.2-1.2.0.jar                    | None                                     |
	| UCHIJAAAA | simplegenerators         | 1.12.2-2.0.11a               | simplegenerators-1.12.2-2.0.11a.jar               | None                                     |
	| UCHIJAAAA | storagenetwork           | 1.12.2-1.2.4                 | SimpleStorageNetwork-1.12.2-1.2.4.jar             | None                                     |
	| UCHIJAAAA | simplyarrows             | 1.0.4                        | SimplyArrows-1.12.2-1.0.4.jar                     | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | spartanshields           | 1.4.1                        | SpartanShields-1.12.2-1.4.1.jar                   | None                                     |
	| UCHIJAAAA | spatialservermod         | 1.3                          | spatialservermod-1.3.jar                          | None                                     |
	| UCHIJAAAA | stevescarts              | 2.4.20.99                    | StevesCarts-1.12.2-2.4.20.99.jar                  | None                                     |
	| UCHIJAAAA | stg                      | 1.12.2-1.2.3                 | stg-1.12.2-1.2.3.jar                              | None                                     |
	| UCHIJAAAA | streams                  | 0.4.4                        | Streams-1.12-0.4.4.jar                            | None                                     |
	| UCHIJAAAA | sasit                    | 1.1.14                       | StuffASockInIt-1.12.2-1.1.14.jar                  | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | supersoundmuffler        | 1.0.2.9                      | supersoundmuffler-1.12.1-1.0.2.9.jar              | None                                     |
	| UCHIJAAAA | tallgates                | 1.0.0                        | TallGates-1.12.2-1.0.0.1.jar                      | None                                     |
	| UCHIJAAAA | beneath                  | 1.4.1                        | The Beneath-1.12.2-1.4.1.jar                      | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
	| UCHIJAAAA | thirstybottles           | 1.1.4                        | ThirstyBottles-1.12.2-1.1.4.jar                   | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | tcomplement              | ${version}                   | TinkersComplement-1.12.2-0.2.3b.jar               | None                                     |
	| UCHIJAAAA | tinkerstages             | 1.0.14                       | TinkerStages-1.12.2-1.0.14.jar                    | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | tinkertoolleveling       | 1.12.2-1.0.5.DEV.30c7957     | TinkerToolLeveling-1.12.2-1.0.5.jar               | None                                     |
	| UCHIJAAAA | tipthescales             | 1.0.1                        | TipTheScales-1.12.2-1.0.1.jar                     | None                                     |
	| UCHIJAAAA | toastcontrol             | 1.6.0                        | Toast Control-1.12.2-1.6.0.jar                    | None                                     |
	| UCHIJAAAA | togetherforever          | 1.0.2                        | togetherforever-1.12.2-1.0.7-13.jar               | None                                     |
	| UCHIJAAAA | tombmanygraves           | @VERSION@                    | TombManyGraves-1.12-4.0.3.jar                     | None                                     |
	| UCHIJAAAA | totemic                  | 1.12.2-0.11.1                | Totemic-1.12.2-0.11.1.jar                         | 21d11d7bf4d97b465382a1f95428029aac6daaea |
	| UCHIJAAAA | tothebatpoles            | 1.12-1.1.0.0                 | tothebatpoles-1.12-1.1.0.0.jar                    | None                                     |
	| UCHIJAAAA | translocators            | 2.5.0.70                     | Translocators-1.12.2-2.5.0.70-universal.jar       | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| UCHIJAAAA | triumph                  | 1.13.0                       | Triumph-1.12.2-1.13.0.jar                         | None                                     |
	| UCHIJAAAA | trumpetskeleton          | 1.12-1.0.2.1                 | trumpetskeleton-1.12-1.0.2.1.jar                  | None                                     |
	| UCHIJAAAA | tumbleweed               | 1.11-0.4.5                   | tumbleweed-1.11-0.4.5.jar                         | None                                     |
	| UCHIJAAAA | twilightforest           | 3.7.424                      | twilightforest-1.12.2-3.7.424-universal.jar       | None                                     |
	| UCHIJAAAA | uppers                   | 0.0.6                        | Uppers-0.0.6.jar                                  | None                                     |
	| UCHIJAAAA | universalmodifiers       | 1.12.2-1.0.9a                | valkyrielib-1.12.2-2.0.11a.jar                    | None                                     |
	| UCHIJAAAA | vc                       | 5.6.1                        | ViesCraft-1.12.2-5.6.1.jar                        | None                                     |
	| UCHIJAAAA | vtt                      | 0.6.4                        | VillagerTrades-1.12-0.6.4.jar                     | None                                     |
	| UCHIJAAAA | waddles                  | 0.6.0                        | Waddles-1.12.2-0.6.0.jar                          | None                                     |
	| UCHIJAAAA | wailastages              | 1.0.22                       | WailaStages-1.12.2-1.0.22.jar                     | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | wanionlib                | 1.12.2-1.5                   | WanionLib-1.12.2-1.5.jar                          | None                                     |
	| UCHIJAAAA | watercontrolextreme      | 1.0.0                        | WaterControlExtreme-1.0.2.jar                     | None                                     |
	| UCHIJAAAA | waterstrainer            | 3.2.0                        | WaterStrainer-1.12-3.2.0.jar                      | None                                     |
	| UCHIJAAAA | wawla                    | 2.5.257                      | Wawla-1.12.2-2.5.257.jar                          | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | weirdinggadget           | 1.0                          | weirdinggadget-1.12.2-2.0.5-universal.jar         | None                                     |
	| UCHIJAAAA | wildcrops                | 1.0.1                        | WildCrops-1.12-1.0.1.jar                          | None                                     |
	| UCHIJAAAA | witherskelefix           | 2.6.0                        | Wither Skeleton Tweaks-1.12.2-2.6.0.jar           | None                                     |
	| UCHIJAAAA | wopper                   | 1.12-r5                      | Wopper-1.12-r5.jar                                | None                                     |
	| UCHIJAAAA | xnet                     | 1.6.9                        | xnet-1.12-1.6.9.jar                               | None                                     |
	| UCHIJAAAA | ynot                     | 0.2.2                        | YNot-0.2.2.jar                                    | None                                     |
	| UCHIJAAAA | yoyos                    | 1.12.2-1.2.2.20              | yoyos_1.12.2-1.2.2.20.jar                         | None                                     |
	| UCHIJAAAA | reauth                   | 3.6.0                        | reauth-3.6.0.jar                                  | daba0ec4df71b6da841768c49fb873def208a1e3 |
	| UCHIJAAAA | justthetips              | 1.12-1.0.1.1                 | justthetips-1.12-1.0.1.1.jar                      | None                                     |
	| UCHIJAAAA | primal_tech              | 0.3.3                        | PrimalTech-0.3.3.jar                              | None                                     |
	| UCHIJAAAA | teslacorelib_registries  | 1.0.14                       | tesla-core-lib-1.12.2-1.0.14.jar                  | None                                     |

	Loaded coremods (and transformers): 
BNBGamingCore (BNBGamingCore-1.12.2-0.8.0.jar)
  com.bloodnbonesgaming.bnbgamingcore.core.BNBGamingCoreClassTransformer
AstralCore (astralsorcery-1.12.2-1.8.10.jar)
  
MicdoodlePlugin (MicdoodleCore-1.12.2-4.0.1.177.jar)
  micdoodle8.mods.miccore.MicdoodleTransformer
CTMCorePlugin (CTM-MC1.12-0.3.0.15.jar)
  team.chisel.ctm.client.asm.CTMTransformer
LoadingPlugin (Quark-r1.4-123.jar)
  vazkii.quark.base.asm.ClassTransformer
Do not report to Forge! Remove FoamFixAPI (or replace with FoamFixAPI-Lawful) and try again. (foamfix-0.9.9.1-1.12.2-anarchy.jar)
  pl.asie.foamfix.coremod.FoamFixTransformer
CorePlugin (SmoothFont-1.12.2-1.15.jar)
  bre.smoothfont.asm.Transformer
CoreMod (Aroma1997Core-1.12.2-1.3.0.2.jar)
  
FarseekCoreMod (Farseek-1.12-2.3.jar)
  farseek.core.FarseekClassTransformer
Inventory Tweaks Coremod (InventoryTweaks-1.64-dev.jar)
  invtweaks.forge.asm.ContainerTransformer
ForgelinPlugin (Forgelin-1.6.0.jar)
  
IELoadingPlugin (ImmersiveEngineering-core-0.12-82.jar)
  blusunrize.immersiveengineering.common.asm.IEClassTransformer
LoadingPlugin (ResourceLoader-MC1.12.1-1.5.3.jar)
  lumien.resourceloader.asm.ClassTransformer
AppleCore (AppleCore-mc1.12.2-3.1.1.jar)
  squeek.applecore.asm.TransformerModuleHandler
IvToolkit (IvToolkit-1.3.3-1.12.jar)
  
BetterFoliageLoader (BetterFoliage-MC1.12-2.1.10.jar)
  mods.betterfoliage.loader.BetterFoliageTransformer
TheBetweenlandsLoadingPlugin (TheBetweenlands-3.3.8-core.jar)
  thebetweenlands.core.TheBetweenlandsClassTransformer
	GL info: ~~ERROR~~ RuntimeException: No OpenGL context found in the current thread.
	Pulsar/tconstruct loaded Pulses: 
		- TinkerCommons (Enabled/Forced)
		- TinkerWorld (Enabled/Not Forced)
		- TinkerTools (Enabled/Not Forced)
		- TinkerHarvestTools (Enabled/Forced)
		- TinkerMeleeWeapons (Enabled/Forced)
		- TinkerRangedWeapons (Enabled/Forced)
		- TinkerModifiers (Enabled/Forced)
		- TinkerSmeltery (Enabled/Not Forced)
		- TinkerGadgets (Enabled/Not Forced)
		- TinkerOredict (Enabled/Forced)
		- TinkerIntegration (Enabled/Forced)
		- TinkerFluids (Enabled/Forced)
		- TinkerMaterials (Enabled/Forced)
		- TinkerModelRegister (Enabled/Forced)
		- chiselIntegration (Enabled/Not Forced)
		- chiselsandbitsIntegration (Enabled/Not Forced)
		- wailaIntegration (Enabled/Not Forced)

	Pulsar/natura loaded Pulses: 
		- NaturaCommons (Enabled/Forced)
		- NaturaOverworld (Enabled/Not Forced)
		- NaturaNether (Enabled/Not Forced)
		- NaturaDecorative (Enabled/Not Forced)
		- NaturaEntities (Enabled/Not Forced)
		- NaturaOredict (Enabled/Forced)
		- NaturaWorld (Enabled/Not Forced)

	AE2 Version: stable rv5-stable-11 for Forge 14.23.1.2554
	Pulsar/tcomplement loaded Pulses: 
		- ModuleCommons (Enabled/Forced)
		- ModuleFeature (Enabled/Not Forced)
		- CeramicsPlugin (Enabled/Not Forced)
		- ChiselPlugin (Enabled/Not Forced)

	List of loaded APIs: 
		* AbyssalCraftAPI (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Biome (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Block (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Caps (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Condition (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Disruption (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Energy (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Entity (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Event (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Integration (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Internal (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Item (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Necronomicon (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Recipe (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Ritual (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* AbyssalCraftAPI|Spell (1.15.0) from AbyssalCraft-1.12.2-1.9.4.9.jar
		* actuallyadditionsapi (33) from ActuallyAdditions-1.12.2-r135.jar
		* antiqueatlasapi (5.1) from antiqueatlas-1.12.2-4.4.9.jar
		* AppleCoreAPI (3.1.0) from AppleCore-mc1.12.2-3.1.1.jar
		* appliedenergistics2|API (rv5) from appliedenergistics2-rv5-stable-11.jar
		* AromaBackupAPI (1.0) from AromaBackup-1.12.2-2.1.1.3.jar
		* Base|API (1.0.0) from base-1.12.2-3.7.2.jar
		* Baubles|API (1.4.0.2) from ImprovedBackpacks-1.12.2-1.2.0.3.jar
		* betteradvancements|API (0.0.7) from Triumph-1.12.2-1.13.0.jar
		* BetterWithModsAPI (Beta 0.6) from BetterWithMods-1.12-2.1.24.jar
		* BetweenlandsAPI (1.10.0) from TheBetweenlands-3.3.8-universal.jar
		* bloodmagic-api (2.0.0) from BloodMagic-1.12.2-2.2.12-97.jar
		* BuildCraftAPI|blocks (1.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|boards (2.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|core (2.2) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|crops (1.1) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|enums (1.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|events (2.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|facades (1.1) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|filler (5.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|fuels (2.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|gates (4.1) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|items (1.1) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|library (2.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|lists (1.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|power (1.3) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|recipes (3.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|robotics (3.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|statements (1.1) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|tiles (1.2) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|tools (1.0) from buildcraft-core-7.99.17.jar
		* BuildCraftAPI|transport (5.0) from buildcraft-core-7.99.17.jar
		* Chisel-API (0.0.1) from Chisel-MC1.12.2-0.2.0.31.jar
		* ChiselAPI|Carving (0.0.1) from Chisel-MC1.12.2-0.2.0.31.jar
		* ChiselsAndBitsAPI (13.8.0) from chiselsandbits-14.17.jar
		* commoncapabilities|api (0.0.1) from CommonCapabilities-1.12-1.4.0.jar
		* ctm-api (0.1.0) from CTM-MC1.12-0.3.0.15.jar
		* ctm-api-events (0.1.0) from CTM-MC1.12-0.3.0.15.jar
		* ctm-api-models (0.1.0) from CTM-MC1.12-0.3.0.15.jar
		* ctm-api-textures (0.1.0) from CTM-MC1.12-0.3.0.15.jar
		* ctm-api-utils (0.1.0) from CTM-MC1.12-0.3.0.15.jar
		* farmingforblockheads|api (1.0) from FarmingForBlockheads_1.12.2-3.1.17.jar
		* Galacticraft API (1.1) from GalacticraftCore-1.12.2-4.0.1.177.jar
		* Guide-API|API (2.0.0) from Guide-API-1.12-2.1.5-60.jar
		* ImmersiveEngineering|API (1.0) from ImmersiveEngineering-0.12-82.jar
		* ImmersiveEngineering|ImmersiveFluxAPI (1.0) from ImmersiveEngineering-0.12-82.jar
		* industrialforegoingapi (5) from industrialforegoing-1.12.2-1.10.0-173.jar
		* integrateddynamics|api (0.2.0) from IntegratedDynamics-1.12.2-0.11.12.jar
		* journeymap|client-api (1.4) from journeymap-1.12.2-5.5.2.jar
		* journeymap|client-api-display (1.4) from journeymap-1.12.2-5.5.2.jar
		* journeymap|client-api-event (1.4) from journeymap-1.12.2-5.5.2.jar
		* journeymap|client-api-model (1.4) from journeymap-1.12.2-5.5.2.jar
		* journeymap|client-api-util (1.4) from journeymap-1.12.2-5.5.2.jar
		* JustEnoughItemsAPI (4.13.0) from jei_1.12.2-4.9.2.196.jar
		* MekanismAPI|core (9.0.0) from Mekanism-1.12.2-9.4.11.346.jar
		* MekanismAPI|energy (9.0.0) from Mekanism-1.12.2-9.4.11.346.jar
		* MekanismAPI|gas (9.0.0) from Mekanism-1.12.2-9.4.11.346.jar
		* MekanismAPI|infuse (9.0.0) from Mekanism-1.12.2-9.4.11.346.jar
		* MekanismAPI|laser (9.0.0) from Mekanism-1.12.2-9.4.11.346.jar
		* MekanismAPI|transmitter (9.0.0) from Mekanism-1.12.2-9.4.11.346.jar
		* MekanismAPI|util (9.0.0) from Mekanism-1.12.2-9.4.11.346.jar
		* MouseTweaks|API (1.0) from MouseTweaks-2.8-mc1.12.1.jar
		* PneumaticCraftApi (1.0) from pneumaticcraft-repressurized-1.12.2-0.6.6-192.jar
		* QuarkAPI (2) from Quark-r1.4-123.jar
		* reborncoreAPI (3.8.7.295) from RebornCore-1.12.2-3.8.7.295-universal.jar
		* reborncoreAPI|Power (3.8.7.295) from RebornCore-1.12.2-3.8.7.295-universal.jar
		* reborncoreAPI|Recipe (3.8.7.295) from RebornCore-1.12.2-3.8.7.295-universal.jar
		* reborncoreAPI|Tile (3.8.7.295) from RebornCore-1.12.2-3.8.7.295-universal.jar
		* stevescartsAPI (${version}) from StevesCarts-1.12.2-2.4.20.99.jar
		* stevescartsAPI|FARMS (${version}) from StevesCarts-1.12.2-2.4.20.99.jar
		* StorageDrawersAPI (2.1.0) from StorageDrawers-1.12.2-5.3.6.jar
		* StorageDrawersAPI|event (2.1.0) from StorageDrawers-1.12.2-5.3.6.jar
		* StorageDrawersAPI|registry (2.1.0) from StorageDrawers-1.12.2-5.3.6.jar
		* StorageDrawersAPI|render (2.1.0) from StorageDrawers-1.12.2-5.3.6.jar
		* StorageDrawersAPI|storage (2.1.0) from StorageDrawers-1.12.2-5.3.6.jar
		* StorageDrawersAPI|storage-attribute (2.1.0) from StorageDrawers-1.12.2-5.3.6.jar
		* togetherforeverapi (1) from togetherforever-1.12.2-1.0.7-13.jar
		* totemic|API (1.12.2-6.3.0) from Totemic-1.12.2-0.11.1.jar
		* valkyrielib.api (1.12.2-2.0.10a) from valkyrielib-1.12.2-2.0.11a.jar
		* WailaAPI (1.3) from Hwyla-1.8.26-B41_1.12.2.jar
	RebornCore: 
		Plugin Engine: 0
		RebornCore Version: 3.8.7.295
		Runtime Debofucsation 1
		RenderEngine: 0
	AE2 Integration: IC2:OFF, RC:OFF, MFR:OFF, Waila:ON, InvTweaks:ON, JEI:ON, Mekanism:OFF, OpenComputers:OFF, THE_ONE_PROBE:OFF, TESLA:OFF, CRAFTTWEAKER:ON
	Profiler Position: N/A (disabled)
	Player Count: 1 / 8; [EntityPlayerMP['KipoPlays'/700, l='Sev Goodness', x=-209.30, y=79.00, z=-223.30]]
	Type: Integrated Server (map_client.txt)
	Is Modded: Definitely; Client brand changed to 'fml,forge'
