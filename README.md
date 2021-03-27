~~~~~~~~~~~~~~~~~~~~~~~~~


*Updated 3/27/2021

*For UE4 games for reference/customization/optimization/learning

*Always testing stuff contact me twitch.tv/smoothschannel or discord


-----------end-----------


Open Engine.ini and copy/paste commands/configs:

Press:       Windows key + R      
Copy/Paste:  %localappdata%/SquadGame/Saved/Config/WindowsNoEditor/Engine.ini 
Copy/Paste:  %localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/Engine.ini


My config:

[Core.Log]
Global=off;

[Audio]
MaxChannels=128; 32-64-96 for PERFORMANCE
CommonAudioPoolSize=32; default 0
UnfocusedVolumeMultiplier=1;

[/Script/Engine.Engine]
bSmoothFrameRate=0;
bPauseOnLossOfFocus=0;
bUseFixedFrameRate=0;
DisplayGamma=2.2;

[TextureStreaming]
PoolSizeVRAMPercentage=70; texturePool cache lower if vram runs too high

[/Script/Engine.StreamingSettings]
s.EventDrivenLoaderEnabled=1;
s.AsyncLoadingThreadEnabled=1;
s.UseBackgroundLevelStreaming=1;

[SystemSettings]
tick.AllowAsyncTickDispatch=1;
tick.DoAsyncEndOfFrameTasks=1;
tick.DoAsyncEndOfFrameTasks.Randomize=1;
AllowAsyncRenderThreadUpdates=1;
AllowAsyncRenderThreadUpdatesDuringGamethreadUpdates=1;
net.AllowAsyncLoading=1;
net.AllowEncryption=1;
net.ProcessQueuedBunchesMillisecondLimit=8;
p.DisableQueryOnlyActors=0;
p.AnimDynamics=0; 0 for PERFORMANCE
p.AnimDynamicsWind=0; 0 for PERFORMANCE
p.AnimDynamicsLODThreshold=0;
p.RagdollPhysics=1;
p.BatchPhysXTasksSize=1;
p.RigidBodyNode=0; 0 for PERFORMANCE
p.RigidBodyLODThreshold=0;
a.Budget.Enabled=1;
a.Budget.BudgetMs=1.5;
FX.BatchAsync=1;
FX.AllowAsyncTick=1;
FX.EarlyScheduleAsync=1;
FX.BatchAsyncBatchSize=32;
FX.AllowCulling=1;
FX.AllowGPUParticles=1;
FX.AllowGPUSorting=1;
FX.MaxCPUParticlesPerEmitter=50;
FX.MaxGPUParticlesSpawnedPerFrame=512;
AudioThread.BatchAsyncBatchSize=32;
AudioThread.UseBackgroundThreadPool=1;
AudioThread.EnableBatchProcessing=1;
r.Atmosphere=1;
r.setres=2560x1440wf; SET YOUR RESOLUTION
r.VSync=0;
r.AllowHDR=0;
r.HDR.EnableHDROutput=0;
r.GPUCrashDebugging=0;
r.XGEShaderCompile=1;
r.CompileShadersForDevelopment=0;
r.CreateShadersOnLoad=1;
r.EarlyZPass=3;
r.EarlyZPassMovable=1;
r.EarlyZPassOnlyMaterialMasking=1;
r.FinishCurrentFrame=0;
r.OneFrameThreadLag=1; 1 game sync with render thread
r.GTSyncType=0;
rhi.SyncSlackMS=0;
r.RHICmdBypass=0;
r.RHICmdBalanceParallelLists=0;
r.D3D11.Depth24Bit=0;
r.DrawRectangleOptimization=1;
r.AlsoUseSphereForFrustumCull=1;
r.MeshStreaming=1;----------------------------test
r.DeferSkeletalDynamicDataUpdateUntilGDME=0; 1 is EXPERIMENTAL
r.DoInitViewsLightingAfterPrepass=0; 1 is EXPERIMENTAL
r.DoLazyStaticMeshUpdate=0; 1 is EXPERIMENTAL
r.DiscardUnusedQuality=0; default 0
r.RenderTargetPoolMin=400;
r.SelectiveBasePassOutputs=1;
r.OptimizeForUAVPerformance=0; faster but uses more gpu memory----------------------------test
r.MorphTarget.Mode=1; 0 cpu method 1 gpu method default 1
r.UseShaderCaching=1;
r.UseShaderPredraw=1;
r.ForwardShading=0;
r.SupportSimpleForwardShading=0;
r.SimpleForwardShading=0;
r.VertexFoggingForOpaque=1;
r.ForceAllCoresForShaderCompiling=0;
r.ShaderComplexity.CacheShaders=1;
r.VirtualTexture=1;
r.VirtualTexturedLightmaps=1;
r.AllowStaticLighting=0;---------------------------------------some games use this if lighting is incorrect turn this on
r.GenerateMeshDistanceFields=1; 0 for PERFORMANCE
r.NormalMapsForStaticLighting=0;
r.DistanceFieldBuild.EightBit=0;
r.GenerateLandscapeGIData=0;
r.DistanceFieldGI=0;
r.DoPrepareDistanceFieldSceneAfterRHIFlush=1;
r.DistanceFieldBuild.Compress=0; 1 for GROUND BRANCH-----------some games will crash without this
r.DBuffer=1; decals 0 for PERFORMANCE
r.AllowGlobalClipPlane=0;
r.LightPropagationVolume=0;
r.HZBOcclusion=1; occlusion culling algorithm default 1
r.AllowOcclusionQueries=1;
r.NumBufferedOcclusionQueries=1;
r.AllowSubPrimitiveQueries=1;
r.MinScreenRadiusForLights=0.03; default 0.03
r.MinScreenRadiusForDepthPrepass=0.03; default 0.03
r.MinScreenRadiusForCSMDepth=0.01;
r.MinScreenRadiusForSmallLights=0.01;
r.SSGI.Enable=0; screen space global illumination
r.SSGI.Quality=0; 0 for PERFORMANCE 1-4 QUALITY VALUES
r.SSGI.HalfRes=0; 1 for PERFORMANCE
r.SSGI.LeakFreeReprojection=1;
r.SceneColorFormat=3; 3 for PERFORMANCE
r.DefaultBackBufferPixelFormat=0; 0 for PERFORMANCE
r.ClearSceneMethod=1;
r.GBufferFormat=1; 1-3 QUALITY VALUES default 1
r.LightFunctionQuality=1; 0 for PERFORMANCE default 2
r.ClearCoatNormal=0; 0 for PERFORMANCE
Compat.UseDXT5NormalMaps=0;
r.SupportLowQualityLightmaps=0;
r.SupportStationarySkylight=1;
r.SkylightIntensityMultiplier=1; lower to darken skylight
r.LightMaxDrawDistanceScale=1; dynamic lights lod scale 0 for PERFORMANCE
r.MipMapLODBias=0; lods
r.LandscapeLODBias=0; 1 for PERFORMANCE
r.SkeletalMeshLODBias=0;
r.ParticleLODBias=-1;
r.ViewDistanceScale=1; view distance 0.8 for PERFORMANCE
r.ViewDistanceScale.SecondaryScale=0; 0 for PERFORMANCE default 1
r.ViewDistanceScale.FieldOfViewAffectsHLOD=0;
r.ViewDistanceScale.FieldOfViewMaxAngle=80;
r.ViewDistanceScale.FieldOfViewMaxAngleScale=1;
r.ViewDistanceScale.FieldOfViewMinAngle=15;
r.ViewDistanceScale.FieldOfViewMinAngleScale=2;
a.URO.Enable=1;
a.URO.ForceAnimRate=0;
a.URO.ForceInterpolation=1;
r.SkeletalMeshLODRadiusScale=1;
r.StaticMeshLODDistanceScale=1; default 1
r.SplineMesh.NoRecreateProxy=1;
r.TextureStreaming=1; texture streaming
r.Streaming.UseBackgroundThreadPool=1;
r.Streaming.PoolSize.VRAMPercentageClamp=1024;
r.Streaming.MaxTempMemoryAllowed=64; default 50
r.Streaming.UseFixedPoolSize=0;
r.Streaming.LimitPoolSizeToVRAM=1;
r.Streaming.PoolSize=2000;
r.Streaming.UseAllMips=0;
r.Streaming.MaxEffectiveScreenSize=0;
r.Streaming.Boost=1;
r.Streaming.MipBias=0;
r.Streaming.UsePerTextureBias=1;
r.Streaming.AmortizeCPUToGPUCopy=1;
r.Streaming.MaxNumTexturesToStreamPerFrame=5;
r.Streaming.NumStaticComponentsProcessedPerFrame=50;
r.Streaming.FullyLoadUsedTextures=0;
r.Streaming.DefragDynamicBounds=1;
r.Streaming.ScaleTexturesByGlobalMyBias=1;
r.Streaming.HiddenPrimitiveScale=0.5; default 0.5----------------------------test
r.Streaming.HLODStrategy=0;
r.Streaming.UseNewMetrics=1;
r.Streaming.MinMipForSplitRequest=1;
r.Streaming.UseMaterialData=1;
r.HLOD=1;
r.HLOD.MaximumLevel=-1;
r.HLOD.DistanceScale=1;
r.HLOD.DistanceOverride=10000;
r.HLOD.ForceDisableCastDynamicShadow=1;
r.DistanceFieldAO=0; 1 for dfao
r.ShadowQuality=4; shadows 0 off
r.Shadow.FilterMethod=0;
r.Shadow.CSM.MaxCascades=2;
r.Shadow.CSM.TransitionScale=1;----------------------------test
r.Shadow.PreShadowResolutionFactor=1; 0.5 for PERFORMANCE
r.Shadow.MaxResolution=1024;
r.Shadow.MaxCSMResolution=2048;
r.Shadow.RadiusThreshold=0.01; 0.03 for PERFORMANCE
r.Shadow.DistanceScale=1; 0.6 for PERFORMANCE
r.Shadow.ForceSingleSampleShadowingFromStationary=0;
r.Shadow.CachePreshadow=1;
r.SupportPointLightWholeSceneShadows=1;
r.Shadow.CacheWholeSceneShadows=1;
r.Shadow.CachedShadowsCastFromMovablePrimitives=1; 0 for PERFORMANCE
r.Shadow.CacheWPOPrimitives=1;
r.Shadow.CSMDepthBias=10;
r.Shadow.FadeExponent=0;
r.Shadow.PreShadowFadeResolution=32;
r.Shadow.MinPreShadowResolution=64;
r.Shadow.FadeResolution=32;
r.Shadow.MinResolution=64;
r.Shadow.TransitionScale=1;
r.Shadow.SpotLightDepthBias=0.03;
r.Shadow.SpotLightReceiverBias=0.03;
r.Shadow.SpotLightSlopeDepthBias=8;
r.Shadow.SpotLightTransitionScale=1;
r.Shadow.MaxNumPointShadowCacheUpdatesPerFrame=2;
r.Shadow.MaxNumSpotShadowCacheUpdatesPerFrame=4;
r.Shadow.PointLightDepthBias=0.03;
r.AllowPointLightCubemapShadows=1;
r.ParallelShadow=1; 0 for PERFORMANCE
r.ParallelShadowsNonWholeScene=0;
r.ContactShadows=0; 0 for PERFORMANCE
r.ContactShadows.NonShadowCastingIntensity=0.2;
r.CapsuleShadows=0;
r.AllowLandscapeShadows=1; landscape shadows 0 for PERFORMANCE
r.DistanceFields=1;
r.DistanceFieldShadowing=1; distance field shadowing 0 for PERFORMANCE
r.DFShadowQuality=1; 1-2 QUALITY VALUES 0 for PERFORMANCE
r.DFFullResolution=0; 0 for PERFORMANCE
r.DFShadowScatterTileCulling=1; 1 is OPTIMAL
r.DFTwoSidedMeshDistanceBias=0;
r.Shadow.MaxNumFarShadowCascades=0;----------------------------test
r.Tonemapper.Quality=2;
r.TonemapperFilm=1;
r.Tonemapper.GrainQuantization=1; 1 for 8bit 0 for 10bit
r.Tonemapper.Sharpen=0;
r.Tonemapper.MergeWithUpscale.Mode=0;
r.MinRoughnessOverride=0; 0.2 with no AA 0 with
r.DefaultFeature.AntiAliasing=2; 1 FXAA 2 TAA 3 MSAA
r.PostProcessAAQuality=3; 0 off 1-2 FXAA 3-4-5-6 TAA
r.MSAA.CompositingSampleCount=1;
r.TemporalAASamples=4;
r.TemporalAAFilterSize=0.25; only works with 6+ TAA samples
r.TemporalAACurrentFrameWeight=0;----------------------------test
r.TemporalAA.R11G11B10History=0; 1 is EXPERIMENTAL
r.TemporalAA.Algorithm=1; Gen 5 TAA
r.TemporalAA.Upsampling=0; allow Gen 5 TAAU
r.TemporalAAUpsampleFiltered=0; 0 for PERFORMANCE
r.SceneRenderTargetResizeMethod=0; 2 uses more memory and can prevent allocation stalls default 0
r.ScreenPercentage=100; lower input res for Gen 4 or 5 TAA use 86.66 or a simple percentage
r.Upscale.Quality=1;
r.Upscale.Softness=0;
r.AmbientOcclusionLevels=2; ssao 0 for PERFORMANCE
r.DefaultFeature.AmbientOcclusionStaticFraction=0; 0 for PERFORMANCE
r.AmbientOcclusionStaticFraction=0; 0 for PERFORMANCE
r.AmbientOcclusionMipLevelFactor=0.6;
r.AmbientOcclusionMaxQuality=75; 75 for PERFORMANCE
r.AmbientOcclusionSampleSetQuality=-1;
r.AmbientOcclusion.Compute=0;
r.AmbientOcclusionRadiusScale=0;
r.LightShaftQuality=0; lightshafts 0 for PERFORMANCE
r.LightShaftDownSampleFactor=0;
r.LightShaftFirstPassDistance=0.1;
r.LightShaftBlurPasses=2;
r.LightShaftNumSamples=1;
r.LightShaftRenderToSeparateTranslucency=1;
r.TranslucencyLightingVolume=1; translucency
r.TranslucencyVolumeBlur=1;
r.TranslucencyLightingVolumeDim=32;
r.SeparateTranslucency=1;
r.SeparateTranslucencyScreenPercentage=100;
r.SeparateTranslucencyAutoDownsample=1;
r.TranslucentSortPolicy=0;
r.CustomDepth=3;
r.CustomDepth.Order=1;
r.CustomDepthTemporalAAJitter=0;
r.SupportSkyAtmosphere=1;
r.SupportSkyAtmosphereAffectsHeightFog=1;----------------------------test
r.SupportAtmosphericFog=1;
r.Fog=1;
r.VolumetricFog=1; 0 for PERFORMANCE
r.VolumetricFog.GridPixelSize=16;
r.VolumetricFog.GridSizeZ=64;
r.VolumetricFog.HistoryWeight=0.9;
r.VolumetricFog.InjectShadowedLightsSeparately=0;
r.VolumetricFog.TemporalReprojection=1;
r.VolumetricFog.HistoryMissSupersampleCount=1;
r.ReflectionEnvironment=1; reflection environment 0 for PERFORMANCE
r.HalfResReflections=1;
r.ReflectionEnvironmentLightmapMixBasedOnRoughness=1;
r.ReflectionEnvironmentBeginMixingRoughness=0.1;
r.ReflectionEnvironmentEndMixingRoughness=0.3;
r.ReflectionEnvironmentLightmapMixing=1;
r.ReflectionEnvironmentLightmapMixLargestWeight=1000;
r.chaos.ReflectionCaptureStaticSceneOnly=1; 1 for PERFORMANCE
r.DoTiledReflections=1; tiled reflection
r.NoTiledReflections=0;
r.ReflectionCaptureGPUArrayCopy=1;
r.ReflectionCaptureResolution=128; default 128
r.TiledDeferredShading=1; tiled deferred shading
r.TiledDeferredShading.MinimumCount=10;----------------------------test
r.SSR.Quality=0; ssr 0 for PERFORMANCE
r.SSR.HalfResSceneColor=1; 1 for PERFORMANCE
r.SSR.MaxRoughness=0.8;
r.SubsurfaceScattering=1; sss 0 for PERFORMANCE
r.SSS.Scale=3;
r.SSS.SampleSet=0;
r.SSS.Quality=0;
r.SSS.HalfRes=1;
r.SSS.Filter=1;
r.SSS.Checkerboard=1;
r.ParticleLightQuality=1; particles 0 for PERFORMANCE
r.ParticleMinTimeBetweenTicks=10;
r.EmitterSpawnRateScale=0.5; 0.25 for PERFORMANCE
r.Emitter.FastPoolEnable=1;
r.DefaultFeature.AutoExposure=0; eye adaptation
r.DefaultFeature.AutoExposure.Method=0;
r.DefaultFeature.AutoExposure.ExtendDefaultLuminanceRange=0;
r.EyeAdaptationQuality=2;
r.UsePreExposure=0;
r.EyeAdaptation.PreExposureOverride=0;
r.MaxAnisotropy=8;
r.SupportMaterialLayers=0;
r.TessellationAdaptivePixelsPerTriangle=9999999; 9999999 for PERFORMANCE 48 for QUALITY
r.MaterialQualityLevel=1; 0 for PERFORMANCE
r.DetailMode=2; 0 for PERFORMANCE
r.RefractionQuality=1; 0 for PERFORMANCE
r.IrisNormal=1; 0 for PERFORMANCE
r.DepthOfFieldQuality=1; dof 0 for PERFORMANCE
r.Filter.SizeScale=1;
r.BloomQuality=3; bloom
r.Bloom.HalfResoluionFFT=0;
r.Bloom.Cross=0;
r.BlurGBuffer=0;
r.MotionBlurQuality=0;
r.FastBlurThreshold=7;
r.LensFlareQuality=2; lens flares 0 for PERFORMANCE
r.SceneColorFringeQuality=0;
r.SceneColorFringe.Max=-1;
grass.DensityScale=0.6;
grass.DisableDynamicShadows=0; 1 for PERFORMANCE
grass.TickInterval=10;
foliage.DensityScale=0.6; 0.6 for PERFORMANCE
foliage.MinVertsToSplitNode=8192;
ShowFlag.Vignette=0;
ShowFlag.SceneColorFringe=0;
r.DefaultFeature.LightUnits=1;


-----------end-----------


Open Input.ini

%localappdata%/SquadGame/Saved/Config/WindowsNoEditor/Input.ini
%localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/Input.ini


Edit input commands copy/paste:

[/Script/Engine.InputSettings] 
bAltEnterTogglesFullscreen=1;
bF11TogglesFullscreen=0; 
bEnableMouseSmoothing=0;
bViewAccelerationEnabled=0;
InitialButtonRepeatDelay=0.1;
ButtonRepeatDelay=0.1;


-----------end-----------


Open GameUserSettings.ini

%localappdata%/SquadGame/Saved/Config/WindowsNoEditor/GameUserSettings.ini
%localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/GameUserSettings.ini


settings in here are in game options, they will overwrite your engine.ini (lame) search your games GameUserSettings.ini to make sure settings are what you want

bUseVSync=0 
FullscreenMode=1
LastConfirmedFullscreenMode=1
PreferredFullscreenMode=1
bUseDynamicResolution=0
AudioQualityLevel=3
LastConfirmedAudioQualityLevel=3
FrameRateLimit=0
MenuFrameRateLimit=0
MaxCSMResolution=2048
MaxAnisotropy=8
ContactShadows=0
PostFX_Saturation=1.200000
PostFX_Sharpness=0.000000
BloomQuality=3
LensFlareQuality=0
AmbientOcclusion=1
AmbientOcclusionStaticFraction=0
AmbientOcclusionLevels=2
AmbientOcclusionRadiusScale=0.000000
HDRDisplayOutputNits=300
AutoExposure=0
EyeAdaptationQuality=0
DistanceFieldShadows=1
TextureStreamPoolSizeStorage=2000
OverrideOptions=(("r.somerandomcommand", (Value=0,bModified=True)),("r.someotherrandomcommand", (Value=0,bModified=False))) ; if you want to override from GameUserSettings.ini


set your scalability groups

[ScalabilityGroups]
sg.ResolutionQuality=100.000000
sg.ViewDistanceQuality=0
sg.AntiAliasingQuality=0
sg.ShadowQuality=0
sg.PostProcessQuality=0
sg.TextureQuality=0
sg.EffectsQuality=0
sg.FoliageQuality=0
sg.ShadingQuality=0


-----------end-----------


Open DeviceProfiles.ini

%localappdata%/SquadGame/Saved/Config/WindowsNoEditor/DeviceProfiles.ini
%localappdata%/GroundBranch/Saved/Config/WindowsNoEditor/DeviceProfiles.ini


Textures or you can just use in game settings (sg.TextureQuality=) copy/paste:

[/Script/Engine.TextureLODSettings]
TextureLODGroups=(Group=TEXTUREGROUP_World,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverag,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_WorldNormalMap,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_WorldSpecular,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_Character,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_CharacterNormalMap,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_CharacterSpecular,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_Weapon,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_WeaponNormalMap,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_WeaponSpecular,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_Vehicle,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_VehicleNormalMap,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_VehicleSpecular,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_Effects,MinLODSize=1,MaxLODSize=512,LODBias=0,MinMagFilter=linear,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_EffectsNotFiltered,MinLODSize=1,MaxLODSize=512,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_Skybox,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_Lightmap,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_Shadowmap,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)
TextureLODGroups=(Group=TEXTUREGROUP_RenderTarget,MinLODSize=1,MaxLODSize=4096,LODBias=0,MinMagFilter=aniso,MipFilter=point,MipGenSettings=TMGS_SimpleAverage,NumStreamedMips=4)


-----------end-----------


for NVIDIA users:

Reset settings "apply let the 3D app decide" then set "use the advanced 3D image settings" then apply, click take me there
Anisotropic filter: 8x  (to make sure its on)
Low latency mode:  off  (lower than ~85% gpu for lowest input lag)
Power management mode:  Prefer max performance
Preferred refresh rate:  Highest available
TF anisotropic sample optimization:  On
TF Negative LOD bias:  Clamp  (allow for performance as stated by nvidia)
Texture filtering quality:  High performance
Vertical sync:  Off


~~~~~~~~~~~~~~~~~~~~~~~~~
