# Configuration

## Set Environmental Variable

For Mac/Linux,

```sh
cd
vi .zshrc #or code .zshrc, anyway open .zshrc with editor of your choice
```

then put in the following lines
```sh
export PYTHONPATH=your_skynet2.0_root/skynet-python
export SKYNET_CONFIG_ROOT=your_skynet2.0_root/skynet-config/skynet
```
For Windows,

Go to control panel and find wherever you change your environment variables and add `your_skynet2.0_root/skynet-python` to your `PYTHONPATH` and a new variable called `SKYNET_CONFIG_ROOT` at `your_skynet2.0_root/skynet-config/skynet`

## Make Private Key
Make a private key for your own .cfg file.
```sh
cd your_sknet2.0_root/skynet-scripts
git checkout v2 
python3 config/make_private_key.py
```
Take a note of _da directory_ where the script puts your PRIVATE_KEY file in.

## Make Your Config File
Make a copy of `your_sknet2.0_root/skynet-config/skynet_db.cfg` into _da directory_ you get from the previous step.


Delete, modify, and, add rows to follow the example below
```cfg
# The key in the PRIVATE_KEY file generated in the previous step
DB_CRYPT_KEY = "your_key_here" 
# Modify directory based on your own project root directory
UNIFIED_ROOT_DIR_PATH = "your_sknet2.0_root/skynet-data/unified/"
DATA_ROOT_DIR_PATH = "your_sknet2.0_root/skynet-data/data/"
RADIO_DATA_ROOT_DIR_PATH = "your_sknet2.0_root/skynet-data/radio"
MASTER_ROOT_DIR_PATH = "your_sknet2.0_root/skynet-data/masters/"
TEMP_ROOT_DIR_PATH = "your_sknet2.0_root/skynet-data/temp/"
SAMPLE_ROOT_DIR_PATH = "your_sknet2.0_root/skynet-data/sample/"
USER_FILES_DIR_PATH = "your_sknet2.0_root/skynet-data/userfiles/"
WORKSPACE_ROOT_DIR_PATH = "your_sknet2.0_root/skynet-data/workspace/"
OPTICAL_SERVER_STATUS_URL = "http://localhost:37690"
RADIO_SERVER_STATUS_URL = "http://localhost:37691"
TELE_STATUS_SERVER_HOST = "localhost"
TELE_STATUS_SERVER_PORT = 29999
JWT_SECRET = None
DB_BACKEND = "mysql+pymysql"
```

## Create File Structure
Create a folder named `skynet-data` under your_sknet2.0_root directory.

And make the following directories inside `skynet-data`
* unified
* data
* radio
* masters
* temp
* sample
* userfiles
* workspace