# Android Kernel Manifests

A repository containing kernel manifests for my custom Android kernels.

## Usage

```sh
sudo apt-get update
sudo apt-get install repo rsync
repo init -u https://android.googlesource.com/kernel/manifest
curl https://raw.githubusercontent.com/apersomany/android_kernel_manifests/refs/heads/main/<manifest of choice> -o .repo/manifests
repo init -u <manifest of choice>
repo sync
tools/bazel build --config=fast //common:kernel_aarch64_dist
```
