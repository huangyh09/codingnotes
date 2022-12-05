# Download data from clould with wget

## One drive
* Source answer from [here](https://unix.stackexchange.com/a/344721). Note, add `&download=1` at the tail of the `URL`.
  ```bash
    wget --no-check-certificate -O FILE_NAME_TO_SAVE "URL&download=1"
  ```

* Example
  ```bash
  wget --no-check-certificate -O test.txt \
    "https://hkuhk-my.sharepoint.com/:t:/g/personal/yuanhua_hku_hk/EQ7DRpMHFgJGpIucV4toyrQBbAJ1d0EYgm2_ySM4oBqkOg?e=jCTDxG&download=1"
  ```
  
## Google drive

## Zenodo
