# Build.prop Tweaks
Add these lines in Build.prop, which is located in system/system. (Some probably is placebo i haven't tested all of them)

### ¬ Enable Zygote preforking
```
persist.device_config.runtime_native.usap_pool_enabled=true
```

### ¬ Enable 4K in YouTube ( Some Regions only, can make UI laggy )
```
sys.display-size=3840x2160
video.accelerate.hw=1
ro.media.enc.jpeg.quality=100
ro.media.dec.jpeg.memcap=8000000
ro.media.enc.hprof.vid.bps=8000000
ro.media.enc.hprof.vid.fps=65
```

### ¬ Enable Launcher in Memory
```
ro.HOME_APP_ADJ=15
ro.FOREGROUND_APP_ADJ=0
ro.VISIBLE_APP_ADJ=4
ro.HIDDEN_APP_MIN_ADJ=7
```

### ¬ Enable Multi User
```
fw.max_users=5
fw.show_multiuserui=1
fw.showhiddenusers=1 
fw.poweruserswitcher=1
```

### ¬ Enable Google Assistant
```
ro.opa.eligible_device=true
```

### ¬ SafetyNET Fix
```
ro.knox.enhance.zygote.aslr=1
```

### ¬  Enable Multi Sim
```
ro.multisim.simslotcount=2
```

### ¬  Disable Knox
```
ro.securestorage.knox=false
```

### ¬  RMM Fix
```
ro.security.vaultkeeper.native=0
```

### ¬  Disable Locating
```
ro.com.google.locationfeatures=0
ro.com.google.networklocation=0
```

### ¬  Enable Secure Storage
```
ro.securestorage.support=false
```

### ¬  Disable OEM Unlock Toggle
```
ro.frp.pst=
```

### ¬  ADB Fix
```
persist.adb.notify=0
persist.service.adb.enable=1
persist.sys.usb.config=mtp,adb
persist.service.debuggable=1
```

### ¬ Enable Fast Dormancy
```
ro.fast.dormancy=1
ro.config.hw_fast_dormancy=1
ro.ril.fast.dormancy.rule=1
ro.semc.enable.fast_dormancy=true
```

### ¬ Force GPU Rendering on 2d Operations
```
debug.sf.hw=1
debug.egl.profiler=1
debug.egl.hw=1
```

### ¬ Call Delay Fix
```
ro.telephony.call.ring.delay=0
ring.delay=0
```

### ¬ Increase Time Duration For WiFi scanning
```
wifi.supplicant_scan_interval=XXX
```

### ¬ Save Battery Without Performance Drop
```
pm.sleep_mode=1
ro.ril.disable.power.collapse=0
wifi.supplicant_scan_interval=180
```

### ¬ Fps cap remover
```
debug.gr.swapinterval=0
ro.fps_enable=1
ro.fps.capsmin=40fps
ro.fps.capsmax=60fps
cpu.fps=60
gpu.fps=60
```

### ¬ Faster Booting
```
ro.config.hw_quickpoweron=true
```

### ¬ Dalvik Virtual Machine Tweaks
```
dalvik.vm.checkjni=false
dalvik.vm.dexopt-data-only=1
dalvik.vm.heapstartsize=5m
dalvik.vm.heapgrowthlimit=48m
dalvik.vm.heapsize=64m
dalvik.vm.verify-bytecode=false
dalvik.vm.execution-mode=int:jit
dalvik.vm.lockprof.threshold=250
dalvik.vm.dexopt-flags=m=v,o=y
dalvik.vm.stack-trace-file=/data/anr/traces.txt
dalvik.vm.jmiopts=forcecopy
```

### ¬ FPS Stabilizer
```
debug.sf.showupdates=0
debug.sf.showcpu=0
debug.sf.showbackground=0
debug.sf.showfps=0
```

### ¬ Enable Vulkan
```
ro.hwui.use_vulkan=1
```

### ¬ Dalvik JIT for Dex
```
debug.usejit=true
```

### ¬ RIL Wakelock Optimization
```
ro.ril.wake_lock_timeout=10000
```

### ¬ Audio Improvements
```
vendor.audio.media.stereo.control=0
persist.audio.dualmic.config=endfire
persist.audio.fluence.mode=endfire
persist.audio.fluence.voicecall=true
persist.vendor.audio.fluence.voicecomm=true
persist.audio.fluence.voicerec=false
persist.audio.fluence.speaker=true
audio.deep_buffer.media=true
vendor.voice.conc.fallbackpath=deep-buffer
ro.media.dec.aud.mp3.enabled=1
ro.media.enc.aud.mp3.enabled=1
ro.media.dec.aud.flac.enabled=1
ro.media.enc.aud.flac.enabled=1
ro.media.dec.aud.wma.enabled=1
ro.media.enc.aud.wma.enabled=1
media.aac_51_output_enabled=true
flac.sw.decoder.24bit.support=true
persist.audio.speaker.dualmode=true
vendor.audio.playback.mch.downsample=true
vendor.audio.use.sw.alac.decoder=true
vendor.audio.use.sw.ape.decoder=true
af.fast_track_multiplier=1
```
