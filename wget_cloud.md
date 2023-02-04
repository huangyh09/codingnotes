# Download data from cloud with wget

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
* One may follow this [source answer](https://medium.com/@acpanjan/download-google-drive-files-using-wget-3c2c025a8b99)

## Zenodo
* Zenodo is well supported. Just add `-O FILE_NAME_TO_SAVE` or remove the `&download=1` suffix:

  ```bash
  wget https://zenodo.org/record/3723681/files/single-cell-genetics/vireo-v0.2.3.zip
  ```

## FTP download
* Example
  ```bash
  wget --mirror --user=YOUR_USER --ask-password ftp://YOURSITE/YOUR_FOLDER[*]
  ```
