# read_roi

[![PyPI version](https://img.shields.io/pypi/v/read_roi.svg?maxAge=2591000)](https://pypi.org/project/read_roi/)

Read ROI files .zip or .roi generated with ImageJ. Code is largely inspired from : http://rsb.info.nih.gov/ij/developer/source/ij/io/RoiDecoder.java.html

## Functions

```python
from read_roi import read_roi_file
from read_roi import read_roi_zip

roi = read_roi_file(roi_file_path)

# or

rois = read_roi_zip(roi_zip_path)
```

## Note

- Some format specifications are not implemented. See RoiDecoder.java for details.
- Most of "normal" ROI file should work.
- Feel free to hack it and send me modifications.

## Changelog

- 31.10.2013 :
    - initial commit

- 16.11.2013 :
    - handle ROIs outside borders
    - can now return negative coordinates

## Requirements

- Python > 2.7 and > 3.4

## Install

`pip install read_roi`

Or you can use Anaconda and `conda-forge` :

```
conda config --add channels conda-forge
conda install read_roi
```

## License

Under BSD license. See [LICENSE](LICENSE).

## Authors

- Hadrien Mary <hadrien.mary@gmail.com>

## How to release a new version

- Modify version number in `pygraphml/__init__.py`
- Commit and push changes
- Make Github release
- Create and upload packages : `python setup.py sdist bdist_wheel uploadl`
