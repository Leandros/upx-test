# upx-test

To get UPX work on 64-bit executables, you need to statically link your executable (do not use the crt dll's), and disable all runtime error checks (cflags=`/GS- /Gs0x7fffffff /guard:cf-` ldflags=`/DYNAMICBASE:NO /HIGHENTROPYVA:NO /GUARD:NO`).
