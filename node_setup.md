# Node Frontend Setup

## Install Nvm and Node 14
Skynet-dashboard requires node 14. The recommanded way to install node 14 and manage different versions of node is through [nvm](https://github.com/nvm-sh/nvm).

After installing nvm

```sh
nvm install 14
nvm use 14
```

## Install node packages
Get into the skynet-dashboard dir
```sh
cd your_sknet2.0_root/skynet-dashboard
npm install
```
You might need to install [Angular CLI](https://angular.io/cli). Version 13.3.7 is proved to be compatible with the project.