ffmpeg4iphone_4.3
=================

FFMpeg for iPhone

PREREQUISITES:
- you have to have XCode4.2 or 4.3 installed on your Mac
- you have to have XCode command line tools installed (can be installed via XCode -> Preferences ->Downloads)
- you have to have git for mac installed.

INSTRUCTIONS and EXPLANATIONS:

- place build script into some directory (say, /tmp/ffbuild), set executable flag on it (by running 'chmod +x ./build)

- run the script. What it will do:

- it will checkout latest version of FFMpeg into FFmpeg directory (you can safely comment this out if you have already checked out FFmpeg into current directory)

- it will try to detect the location of your Xcode.app and will exit if Xcode is not installed

- it will try to locate gcc inside of the Xcode.app and will exit if it's not found (this may happen if Xcode Command Tools are not installed)

if the above steps ran smoothly, script will

- create build_results folder
- will subsequently run FFmpeg configure and make for 3 different architectures (armv6, armv7, i386) and will put them into respective directories inside of build_results folder
- will run lipo and create universal libs (and will put them inside build_results/Universal) folder.
