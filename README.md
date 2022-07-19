# Skynet2.0-Docs
Bunch of docs for Skynet 2.0 Dev

## Installation

### Step 0 Clone Repos
Read [ME](clone_repos.md)

### Step 1 Set Up Python Environment
Read [ME](python_environment.md)

### Step 2 Configure Project
Read [ME](configuration.md)

### Step 3 Initialize Database
Read [ME](create_db.md)

### Step 4 Prepare Node/Angular
Read [Me](node_setup.md)

## Run the Thing(s?)
1. Fire up Mariadb and Redis services, more details in [create_db.md](create_db.md).

2. Start the frontend angular application
```sh
cd your_sknet2.0_root/skynet-dashboard
npm run start
```
3. Activate your python virtual environment, more details in [python_environment.md](python_environment.md)

4. Run dashboard-api
```sh
cd your_sknet2.0_root/skynet-dashboard-api
python3 run.py
```

5. Run skynet-api
```sh
cd your_sknet2.0_root/skynet-api
python3 run.py
```
6. Go to [http://localhost:4200](http://localhost:4200) and you are good to go!
Default sign in username: admin, password: password
