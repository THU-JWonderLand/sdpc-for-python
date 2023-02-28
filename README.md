# About sdpc-for-python

Sdpc-for-python is a python library for processing whole slide images (WSIs) in **sdpc** format. To read WSIs in sdpc format in Windows platform, download the [TEKSQRAY reading software](https://www.sqray.com/yprj).

|  Download link |  Extraction code |
|  ----  | ----  |
| [Baidu Cloud](https://pan.baidu.com/s/1A4oOSlS2pCTsSRmQ_eCljQ)  | sq12 |

# Installation

|  Platform   |  PyPI installer |
|  ----  | ----  |
| Windows  | `pip install sdpc-win` |
| Linux  | `pip install sdpc-linux`|

# Source Code for sdpc-win & sdpc-linux

[sdpc for linux (version 1.5)](https://pypi.org/project/sdpc-linux/#files)

[sdpc for windows (version 3.0)](https://pypi.org/project/sdpc-win/#files)

# How to use Sdpc library

- **Import Sdpc Library:**

```
from sdpc.Sdpc import Sdpc
```

- **Read WSI**

```
wsi = Sdpc(wsi_path)
```

- **Get the number of levels of WSI**

```
level_count = wsi.level_count
```

- **By how much are levels downsampled from the original image?**

```
level_downsamples = wsi.level_downsample
```

- **Get the dimensions of data in each level**

```
level_dimensions = wsi.level_dimensions
```

- **Get the patch under a certain position at a certain level in WSI**

```
img = wsi.read_region((Position_X, Position_Y), patch_level, (size_H, size_W))   # patch_size = (size_H, size_W)
```

# Batch patches

Build patches from WSIs in sdpc format in [Build-patch-for-sdpc Library](https://github.com/RenaoYan/Build-Patch-for-Sdpc).

Two approaches (build *w/wo* .sdpl) to build patches are given for two different platforms (Windows/Linux).


# Troubleshooting

1. `OSError: libDecodeHevc.so: cannot open shared object file: No such file or directory`

See the issue [#2](https://github.com/WonderLandxD/sdpc-for-python/issues/2).

*H&G Pathology AI Research Team*
