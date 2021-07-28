# libdsm-0.3.2-cust
This is a fork of https://github.com/videolabs/libdsm, version 0.3.2.

Customization is to support download media files from [SMB](https://en.wikipedia.org/wiki/Server_Message_Block) server, together with vlc-android.

## Please follow below steps to take effect.

1. cp /root/mit/libdsm-0.3.2/src/smb_file.c /root/vlc-android/vlc/contrib/contrib-android-arm-linux-androideabi/libdsm/src/smb_file.c
2. touch /root/vlc-android/vlc/contrib/contrib-android-arm-linux-androideabi/libdsm
3. cd /root/vlc-android
4. buildsystem/compile.sh -a armeabi-v7a --release -b
5. APK /root/vlc-android/vlc/build-android-arm-linux-androideabi/ndk/libs/armeabi-v7a/libvlc.so

## Below is an earlier way to take effect.
1. upload smb_file.c to /root/vlc-android/vlc/contrib/contrib-android-aarch64-linux-android/libdsm/src/smb_file.c
2. cd /root/vlc-android/vlc/contrib/contrib-android-aarch64-linux-android/libdsm
3. make clean
4. cd /root/vlc-android
5. ./compile-libvlc.sh -a arm64 signrelease
