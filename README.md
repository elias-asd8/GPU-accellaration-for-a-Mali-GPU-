# GPU-accellaration-for-a-Mali-GPU-
Yes I dealt the struggle too here's a working guide on how to get GPU accellaration on a Mali gpu, I actually tested it on my non rooted nothing phone 2a

# Step 1: X11
we need to get a X11 Display running first.
Heres the cmd
```bash
termux-x11 :0 -ac &
```
we use the -ac flag so its allowed to connect with anything that needs a display.
# Step 2
this is the important bit. copy this block or put this in ur ~/.bashrc or in ur ~/.zshrc:
```bash
export DISPLAY=:0
export EGL_PLATFORM=x11
export LIBGL_ALWAYS_INDIRECT=0
export GALLIUM_DRIVER=panfrost
```
# DONE.
have fun and hope this works!
