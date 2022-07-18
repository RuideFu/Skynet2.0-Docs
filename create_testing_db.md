# Skynet2.0 Create/Recreate Testing Database

__Reed Fu, Created on July 18th, 2022__

## Install & Open Mariadb
Download maridab in your prefered way. Then open mariadb in cml. For Mac/Linux just go straight to terminal. In Windows, search Mariadb in start and run it as an admin.

Then run the following command
```zsh
mariadb -u root -p
```

## Make || Clear Your DB
After logging into Mariadb
```SQL
DROP DATABASE sky; --if you've created a database named sky before
CREATE DATABASE sky; --create the database
```

## Update Your Local Repos
`git pull` the following repos:
* skynet-python
* skynet-scripts (v2 branch)
* skynet-dashboard-api

## Run the Script to Create Testing DB
```zsh
cd your_sknet2.0_root/skynet-scripts/testing/v2
python3 create_test_database.py
```

## Reload Catalogs
```zsh
cd your_sknet2.0_root/skynet-scripts/catalogs
python major_solar_system_init.py
python norad_update.py
python mpc_comet_update.py
python mpc_orbit_update.py
```