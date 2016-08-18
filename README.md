# WebRTC Audio processing standalone module

As you know, webrtc has a lot of audio processing module for VAD, NS and so on, but it cannot be used directly from the source code provided by webrtc.

I extract the VAD module now and I might make the rest of them available in the future.

# How to build

```
mkdir build & cd build
cmake ..
make
```

# How to install

I wrap the install marco in the CMakeLists.txt. But actually it is far from perfect.

You need to update pkg-config in /usr/local/lib to make sure  pkg-config --libs webrtcaudio returns the correct CFLAGS and LIBS.
