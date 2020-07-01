~~~~~~~~~~~~~~~~~~~~~~~~~


*Updated 7/1/2020
*For UE4 games for reference/customization/optimization/learning
*Always testing stuff contact me twitch.tv/smoothschannel or discord


-----------end-----------


Open Engine.ini and Copy/Paste commands/configs:

Press:       Windows key + R      
Copy/Paste:  %localappdata%/SquadGame/Saved/Config/WindowsNoEditor/Engine.ini 
Copy/Paste:  %localappdata%/PostScriptum/Saved/Config/WindowsNoEditor/Engine.ini 
Copy/Paste:  %localappdata%/Insurgency/Saved/Config/WindowsClient/Engine.ini 


-----------end-----------


Squad* PS* Sandstorm* other UE4 games* My config Copy/Paste this:

[Core.Log]
Global=all off ;

[TextureStreaming]
PoolSizeVRAMPercentage=40 ;

[SystemSettings]
r.MSAACount=0 ;
r.VSync=0 ;
r.AllowHDR=0 ;
r.FinishCurrentFrame=0 ;
r.OneFrameThreadLag=1 ;
r.FullScreenMode=0 ;
r.GTSyncType=0 ;
r.GPUCrashDebugging=0 ;
r.HighQualityLightMaps=1 ;
r.DiscardUnusedQuality=1 ;
r.SceneColorFormat=3 ;
r.VirtualTexture=1 ; 0 for PERFORMANCE
ShowFlag.Tessellation=0 ;
r.TessellationAdaptivePixelsPerTriangle=9999999 ;
r.TextureStreaming=1 ;
r.RenderTargetPoolMin=400 ; 300 for PERFORMANCE
r.Streaming.LimitPoolSizeToVRAM=1 ;
r.Streaming.UseFixedPoolSize=0 ;
r.Streaming.PoolSize=1000 ; 400 for PERFORMANCE
r.Streaming.UseAllMips=0 ;
r.Streaming.HLODStrategy=0 ;
r.Streaming.MipBias=0 ; 1 for PERFORMANCE
r.Streaming.UsePerTextureBias=1 ;
r.Streaming.AmortizeCPUToGPUCopy=1 ;
r.Streaming.MaxNumTexturesToStreamPerFrame=0 ;
r.Streaming.NumStaticComponentsProcessedPerFrame=50 ;
r.Streaming.Boost=1 ;
r.Streaming.FullyLoadUsedTextures=0 ;
r.Streaming.MaxEffectiveScreenSize=0 ;
r.Streaming.DefragDynamicBounds=1 ;
r.Streaming.DropMips=2 ;
r.MaxAnisotropy=8 ; 0 for PERFORMANCE
r.MipMapLODBias=0 ;
r.LandscapeLODBias=0 ; 1 for PERFORMANCE
r.SkeletalMeshLODBias=0 ; 1 for PERFORMANCE
r.ParticleLODBias=0 ; 1 for PERFORMANCE
r.SkeletalMeshLODRadiusScale=1 ;
r.StaticMeshLODDistanceScale=1 ;
r.ShadowQuality=3 ;
r.Shadow.PerObject=1 ;
r.Shadow.FilterMethod=0 ;
r.Shadow.CSM.MaxCascades=4 ;
r.Shadow.MaxResolution=1024 ;
r.Shadow.MaxCSMResolution=2048 ;
r.Shadow.RadiusThreshold=0.04 ;
r.Shadow.DistanceScale=0.85 ;
r.Shadow.CSM.TransitionScale=0.8 ;
r.Shadow.PreShadowResolutionFactor=0.5 ;
r.Shadow.CSMDepthBias=10 ; 25 for PS
r.Shadow.CachedShadowsCastFromMovablePrimitives=0 ;
r.AllowLandscapeShadows=1 ; 0 for PERFORMANCE
r.ContactShadows=0 ;
r.CapsuleShadows=0 ;
r.AllowStaticLighting=0 ; 0 for PERFORMANCE 1 for SANDSTORM
r.NormalMapsForStaticLighting=0 ;
Compat.UseDXT5NormalMaps=0 ;
r.ScreenPercentage=100 ;
r.SceneRenderTargetResizeMethod=0 ;
r.Upscale.Quality=3 ;
r.TemporalAASamples=4 ;
r.TemporalAACurrentFrameWeight=0.2 ;
r.TemporalAA.AllowDownsampling=0 ;
r.TemporalAA.Upsampling=0 ;
r.TemporalAAUpsampleFiltered=1 ;
r.Tonemapper.Quality=3 ;
r.TonemapperFilm=1 ;
r.Tonemapper.GrainQuantization=1 ;
r.GenerateMeshDistanceFields=1 ; 0 for PERFORMANCE
r.DistanceFieldShadowing=1 ; 0 for PERFORMANCE
r.DFFullResolution=0 ;
r.DFShadowQuality=1 ;
r.GenerateLandscapeGIData=0 ; 0 for PERFORMANCE
r.AOSpecularOcclusionMode=1 ;
r.AOApplyToStaticIndirect=0 ;
r.DistanceFieldAO=0 ;
r.AOQuality=0 ;
r.DefaultFeature.AmbientOcclusionStaticFraction=0 ;
r.AmbientOcclusionMipLevelFactor=0.4 ;
r.AmbientOcclusionMaxQuality=100 ; 0 for PERFORMANCE
r.AmbientOcclusionLevels=2 ; 0 for PERFORMANCE
r.AmbientOcclusion.Compute=0 ;
r.AmbientOcclusionRadiusScale=0.01 ;
r.ReflectionEnvironment=1 ; 0 for PERFORMANCE
r.ViewDistanceScale=1 ; 0.8 for PERFORMANCE
r.ViewDistanceScale.FieldOfViewAffectsHLOD=0 ; 0 for PERFORMANCE 1 for SANDSTORM
r.HLOD=0 ; 0 for PERFORMANCE 1 for SANDSTORM
r.HLOD.MaximumLevel=-1 ;
r.HLOD.DistanceScale=1 ;
r.HLOD.DistanceOverride=10000 ;
r.LightFunctionQuality=1 ; 0 for PERFORMANCE
r.LightMaxDrawDistanceScale=1 ; 0.8 for PERFORMANCE
r.LightShaftQuality=1 ; 0 for PERFORMANCE 0 for SANDSTORM
r.LightShaftDownSampleFactor=-1 ;
r.LightShaftFirstPassDistance=0.02 ;
r.TranslucencyLightingVolume=1 ;
r.TranslucencyVolumeBlur=1 ;
r.TranslucencyLightingVolumeDim=64 ;
r.VolumetricFog=0 ;
grass.DensityScale=0.6 ;
foliage.DensityScale=0.6 ;
r.SSR.Quality=0 ;
r.SSR.MaxRoughness=0.8 ;
r.MaterialQualityLevel=1 ; 0 for PERFORMANCE
r.SupportMaterialLayers=0 ;
r.SubsurfaceScattering=1 ; 0 for PERFORMANCE
r.SSS.Scale=1 ;
r.SSS.SampleSet=1 ;
r.SSS.Quality=0 ;
r.SSS.HalfRes=1 ;
r.SSS.Filter=1 ;
r.SSS.Checkerboard=2 ;
r.DetailMode=2 ; 0 for PERFORMANCE
r.RefractionQuality=1 ; 0 for PERFORMANCE
r.ParticleLightQuality=1 ; 0 for PERFORMANCE
r.ParticleMinTimeBetweenTicks=8 ; 16 for PERFORMANCE
r.EmitterSpawnRateScale=0.5 ; 0.25 for PERFORMANCE
r.LensFlareQuality=0 ;
r.MotionBlurQuality=0 ;
r.BloomQuality=3 ; 0 for PERFORMANCE
r.Filter.SizeScale=1 ; 0 for PERFORMANCE
r.DepthOfFieldQuality=0 ;
r.SceneColorFringeQuality=1 ; 0 for PERFORMANCE 0 for SANDSTORM
r.SceneColorFringe.Max=0.25 ;
r.EyeAdaptationQuality=2 ; 0 for PERFORMANCE
r.DefaultFeature.AutoExposure.Method=1 ;


-----------end-----------


Open GameUserSettings.ini:

Press:       Windows key + R      
Copy/Paste:  %localappdata%/SquadGame/Saved/Config/WindowsNoEditor/GameUserSettings.ini
Copy/Paste:  %localappdata%/Insurgency/Saved/Config/WindowsClient/GameUserSettings.ini 
Copy/Paste:  %localappdata%/PostScriptum/Saved/Config/WindowsNoEditor/GameUserSettings.ini 


Resets when you change in game for squad/ps devs dont do this, also check this 
in your games because it will overwrite engine.ini changes:

MSAACompositingSampleCount=1
BloomQuality=3 
LensFlareQuality=2 
AmbientOcclusion=1
AmbientOcclusionStaticFraction=0
AmbientOcclusionLevels=1 
AmbientOcclusionRadiusScale=0.010000 
AutoExposure=1
EyeAdaptationQuality=2


Set these to what you want:

[ScalabilityGroups]
sg.ResolutionQuality=100.000000
sg.ViewDistanceQuality=0
sg.AntiAliasingQuality=3
sg.ShadowQuality=0
sg.PostProcessQuality=0
sg.TextureQuality=0
sg.EffectsQuality=0
sg.FoliageQuality=0


Other commands to test some devs forget to turn off mouse smoothing in games:

FullscreenMode=0
bAltEnterTogglesFullscreen=1
bF11TogglesFullscreen=0
bUseDynamicResolution=0
bPauseOnLossOfFocus=0
bUseFixedFrameRate=0
bEnableMouseSmoothing=0
bEnableFrameRateSmoothing=0
bSmoothFrameRate=0
bUseVSync=0 
FrameRateLimit=144.000000
AudioQualityLevel=3


-----------end-----------


EXTRA* For NVIDIA users in control panel change:

Low latency mode:  off  (lower than ~85% gpu for lowest input lag)
Power management mode:  Prefer max performance
Preferred refresh rate:  Highest available
TF anisotropic sample optimization:  off (on for PERFORMANCE) 
TF Negative LOD bias:  Allow
Texture filtering quality:  High performance (Quality for newer GPUs)
Vertical sync:  Off


~~~~~~~~~~~~~~~~~~~~~~~~~
