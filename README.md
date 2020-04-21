# font_problem

A minimal repo to reproduce the [App crashed while setting font](https://github.com/flutter/flutter/issues/33337) error

Error occurs on Virtual Device (Pixel 2):

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

Error when trying to load it onto OnePlus 5T:

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
