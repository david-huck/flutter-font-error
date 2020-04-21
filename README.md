# font_problem

A minimal repo to reproduce the [App crashed while setting font](https://github.com/flutter/flutter/issues/33337) error

## Error occurs on Virtual Device (Pixel 2):

    D/EGL_emulation( 8625): eglMakeCurrent: 0xec6c2a40: ver 2 0 (tinfo 0xec6f32a0)
    D/eglCodecCommon( 8625): setVertexArrayObject: set vao to 0 (0) 1 0
    E/flutter ( 8625): [ERROR:flutter/third_party/txt/src/minikin/FontFamily.cpp(184)] Could not get cmap table size!
    E/flutter ( 8625):
    F/flutter ( 8625): [FATAL:flutter/third_party/txt/src/minikin/FontCollection.cpp(95)] nTypefaces == 0
    F/libc    ( 8625): Fatal signal 6 (SIGABRT), code -6 (SI_TKILL) in tid 8661 (1.ui), pid 8625 (le.font_problem)
    *** *** *** *** *** *** *** *** *** *** *** *** *** *** *** ***
    Build fingerprint: 'google/sdk_gphone_x86_arm/generic_x86_arm:9/PSR1.180720.117/5875966:user/release-keys'
    Revision: '0'
    ABI: 'x86'
    pid: 8625, tid: 8661, name: 1.ui  >>> com.example.font_problem <<<  
    signal 6 (SIGABRT), code -6 (SI_TKILL), fault addr --------
    Abort message: '[FATAL:flutter/third_party/txt/src/minikin/FontCollection.cpp(95)] nTypefaces == 0
    '
    eax 00000000  ebx 000021b1  ecx 000021d5  edx 00000006
    edi 000021b1  esi 00000060
    ebp d66bf7c8  esp d66bf768  eip f5bb2b39
    backtrace:
    #00 pc 00000b39  [vdso:f5bb2000] (__kernel_vsyscall+9)
    #01 pc 0001fdf8  /system/lib/libc.so (syscall+40)
    #02 pc 00022ed3  /system/lib/libc.so (abort+115)
    #03 pc 0115a7f7  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #04 pc 0147ee90  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #05 pc 0147f030  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #06 pc 0148b452  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #07 pc 0148b3f4  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #08 pc 01489c11  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #09 pc 0148f0ec  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #10 pc 0148ea2a  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #11 pc 0149005d  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #12 pc 01185080  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #13 pc 0116a8ca  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #14 pc 0116a873  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #15 pc 01184c77  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #16 pc 01648f7b  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #17 pc 01648ee3  /data/app/com.example.font_problem-rFxM3Vpz1e38QCJyda_LqA==/lib/x86/libflutter.so (offset 0x113f000)
    #18 pc 000007d3  <anonymous:d5600000>
    Lost connection to device.

## Error when trying to load it onto OnePlus 5T:

    E/flutter ( 9091): [ERROR:flutter/third_party/txt/src/minikin/FontFamily.cpp(184)] Could not get cmap table size!
    E/flutter ( 9091):
    F/flutter ( 9091): [FATAL:flutter/third_party/txt/src/minikin/FontCollection.cpp(95)] nTypefaces == 0
    F/libc    ( 9091): Fatal signal 6 (SIGABRT), code -6 (SI_TKILL) in tid 9137 (1.ui), pid 9091 (ayout_challange)
    *** *** *** *** *** *** *** *** *** *** *** *** *** *** *** ***
    Build fingerprint: 'OnePlus/OnePlus5T/OnePlus5T:9/PKQ1.180716.001/2002242012:user/release-keys'
    Revision: '0'
    ABI: 'arm64'
    pid: 9091, tid: 9137, name: 1.ui  >>> com.example.brewery_layout_challange <<<
    signal 6 (SIGABRT), code -6 (SI_TKILL), fault addr --------    x8  0000000000000083  x9  c6dca50057a63099  x10 0000000000000000  x11 fffffffc7ffffbdf
    x12 0000000000000001  x13 0000000000000028  x14 ffffffffffffffff  x15 0000d52365294d76
    x16 00000075228642a8  x17 0000007522783954  x18 0000000000000010  x19 0000000000002383
    x20 00000000000023b1  x21 0000007480a15f28  x22 0000007496679a28  x23 0000007496679a40
    x24 0000000000000000  x25 0000000000000001  x26 0000007480a160a0  x27 0000000000000000
    x28 0000000000000010  x29 0000007480a15f10
    sp  0000007480a15ed0  lr  0000007522777084  pc  00000075227770ac
    backtrace:
    #00 pc 00000000000220ac  /system/lib64/libc.so (abort+116)
    #01 pc 0000000001225258  /data/app/com.example.brewery_layout_challange-BUJ4RP98_WBhbaZXmMcrEA==/lib/arm64/libflutter.so (offset 0x1210000)
    #02 pc 00000000014969b8  /data/app/com.example.brewery_layout_challange-BUJ4RP98_WBhbaZXmMcrEA==/lib/arm64/libflutter.so (offset 0x1210000)
    #03 pc 00000000014a0e3c  /data/app/com.example.brewery_layout_challange-BUJ4RP98_WBhbaZXmMcrEA==/lib/arm64/libflutter.so (offset 0x1210000)
    #04 pc 000000000149fb08  /data/app/com.example.brewery_layout_challange-BUJ4RP98_WBhbaZXmMcrEA==/lib/arm64/libflutter.so (offset 0x1210000)
    #05 pc 00000000014a3f78  /data/app/com.example.brewery_layout_challange-BUJ4RP98_WBhbaZXmMcrEA==/lib/arm64/libflutter.so (offset 0x1210000)
    #06 pc 00000000014a3a70  /data/app/com.example.brewery_layout_challange-BUJ4RP98_WBhbaZXmMcrEA==/lib/arm64/libflutter.so (offset 0x1210000)
    #07 pc 00000000014a4ac8  /data/app/com.example.brewery_layout_challange-BUJ4RP98_WBhbaZXmMcrEA==/lib/arm64/libflutter.so (offset 0x1210000)
    #08 pc 0000000001230b5c  /data/app/com.example.brewery_layout_challange-BUJ4RP98_WBhbaZXmMcrEA==/lib/arm64/libflutter.so (offset 0x1210000)
    #09 pc 0000000001613d38  /data/app/com.example.brewery_layout_challange-BUJ4RP98_WBhbaZXmMcrEA==/lib/arm64/libflutter.so (offset 0x1210000)
    #10 pc 0000000000001744  <anonymous:000000747ee80000>
    Lost connection to device.
    Exited (sigterm)
