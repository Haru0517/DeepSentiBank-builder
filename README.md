# DeepSentiBank-Builder
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Make the executable file (`extract_nfeatures`) for [DeepSentiBank](https://github.com/generalmilk/DeepSentiBank) in [Caffe](https://github.com/BVLC/caffe).

## Requirement
- [Docker](https://www.docker.com/)
  - docker-compose

## Usage
- Run `docker-compose build`.
- Run `docker-compose up -d`.

You can get the executable file (`extract_nfeatures`) in source folder.

## Run DeepSentiBank
### Test in docker

You can test creating json in this builder project.

After running the following command, `test_image.json` file will be output to source/DeepSentibank folder.
- Run `docker-compose exec builder sh test.sh`.

### Test in your project
Download `caffe_sentibank_train_iter_250000` file from [HERE](https://www.dropbox.com/s/lv3p67m21kr3mrg/caffe_sentibank_train_iter_250000?dl=1).

Then, add `extract_nfeatures` and `caffe_sentibank_train_iter_250000` file to your [DeepSentiBank](https://github.com/generalmilk/DeepSentiBank) folder, and run `python sentiBank.py test_image.jpg`. 

You can get output json file: `test_image.json`.



## Note
#### (2020.01.24) 
Original `extract_nfeatures.cpp` in [DeepSentiBank](https://github.com/generalmilk/DeepSentiBank) contains a bug caused by [Caffe](https://github.com/BVLC/caffe) updates. (Look this [Issue](https://github.com/BVLC/caffe/issues/4107).)

So we use a modified file (`source/extract_nfeatures.cpp`) instead of the original one.

#### (2021.07.15) 
The source of `caffe_sentibank_train_iter_250000` download link is [HERE](https://github.com/ColumbiaDVMM/ColumbiaImageSearch/blob/1326ee97ac1f032fdfbd5245c8356f59b254a9b5/cufacesearch/cufacesearch/featurizer/sbcmdline_img_featurizer.py#L18).

If the download link is broken, please contact me as I have a backup.



# License
This software is released under the MIT License, see LICENSE.

Copyright (c) 2020 Yuto Chikazawa.
