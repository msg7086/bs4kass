It extracts ARIB STD-B69 subtitle from 4K/8K TV Program and converts it to Advanced SubStation Alpha (ASS) file.

## Compiling

Link with avcodec, avformat, avutil and expat.

If manually compiling ffmpeg, use the following flags.

    ./configure --disable-pthreads --disable-bzlib --disable-iconv --disable-lzma --disable-xlib --disable-everything --disable-network --disable-programs --disable-doc --disable-avdevice --disable-swresample --disable-swscale --disable-postproc --disable-avfilter --enable-protocol=file --enable-demuxer=mpegts ...
