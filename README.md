# sublime-platform
- Manifest repository - kas, yocto, beaglebone black
- Reference: github.com/bootlin/simplest-yocto-setup

## Operation
```bash
# If you don't have kas yet (needed once only):
pip install kas

git clone git@github.com:TSMotter/sublime-platform.git
cd sublime-platform

# Use kas to download the third-party repositories needed
# (required the first time, or after changes to .config.yaml)
kas checkout

# Initialize the build environment
. openembedded-core/oe-init-build-env

# Run your first build
bitbake motter-image-minimal

# Have dinner

# Find the output images here
ls -l tmp-glibc/deploy/images/dogbonedark/

# Flash the image (use your uSD card device instead of XYZ!):
sudo bmaptool copy tmp-glibc/deploy/images/dogbonedark/motter-image-minimal-dogbonedark.wic /dev/XYZ
```
