# kestrel-ffmpeg

The FFmpeg builds [Kestrel](https://github.com/isaacbadeau/kestrel) links against, kept
here so every Kestrel build uses exactly the same FFmpeg, for as long as Kestrel needs it.
Nothing is built here: each release holds an unmodified archive from
[BtbN/FFmpeg-Builds](https://github.com/BtbN/FFmpeg-Builds), whose own archives are pruned
over time.

| Release | Archive | SHA-256 |
|---|---|---|
| `ffmpeg-n9.0` | `ffmpeg-n9.0-win64-lgpl-shared.zip` (BtbN `ffmpeg-n9.0-latest-win64-lgpl-shared-9.0`) | `1f4ca60af841829e054b002a729f0c1acb90497e3bc798cb16d4b1f4912da143` |

Kestrel's `mise run ffmpeg` downloads the release's archive, checks that checksum and the
checksum of every DLL, and unpacks it into `third_party/ffmpeg`.

## Licence

FFmpeg is licensed under the GNU Lesser General Public License 3.0 (LGPL) in these
builds (the "lgpl" variant: no GPL components); the licence texts are inside each archive.
The source of FFmpeg n9.0 is at https://ffmpeg.org/download.html and the build scripts at
https://github.com/BtbN/FFmpeg-Builds. This repository adds nothing to them.
