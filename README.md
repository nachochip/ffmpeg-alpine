This takes the ffmpeg binaries that were compiled in ffmpeg-build and 
places them inside a base Alpine container with added glibc.  Size 
is much smaller (~56MB in this container vs ~360MB in the original 
debian container vs ~129MB in an empty base debian).

Example command
docker run nachochip/ffmpeg-alpine -i INPUT -vcodec copy -acodec copy - > OUTPUT.mp4

This container uses the entrypoint="ffmpeg"
