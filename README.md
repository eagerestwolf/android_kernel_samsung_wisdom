# Kernel Sources for Samsung Galaxy A 8.0 LTE (2019)

> ## DISCLAIMER
> I do not own these sources. They came from the
> [Samsung Open Source](https://opensource.samsung.com) website. All of the
> rights to this code belong to Samsung.

## SM-P205
To add these sources to an existing build (ROM, recovery, etc.), add the
following to `.repo/local_manifests/wisdomub.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project name="eagerestwolf/android_kernel_samsung_wisdomub" path="kernel/samsung/wisdomub" remote="github" revision="android-9.0" />
</manifest>
```
Then run `repo sync` to check it out.

---

To build only the kernel, edit the `Makefile` and change `CROSS_COMPILE` to point to your toolchain. Then:
```
export ANDROID_MAJOR_VERSION=p
make ARCH=arm64 exynos7885-wisdom_defconfig
make ARCH=arm64
```

---

To build as part of a ROM, recovery, etc:
```js
// Instructions coming soon!
```

Device source: https://github.com/eagerestwolf/android_device_samsung_wisdomub/
