EOS producer
===
This docker image is for EOS producer. This node is depended on fibos which is side chain of eos and compatible with eos net.
# Depends on
* docker
* docker-compose
# How to start?
## Clone project
open a bash terminal, and run following command
```
git clone https://github.com/fouvy/docker-fibos-eosio-producer.git
```
change current directory to project
```
cd docker-fibos-eosio-producer
```
## Config your information
The config file is fibos/config/config_producer.js and find the config params which start with xxxx, change it to your own information. 
If your haven't register producer, you should register producer first.
### Register producer(optional)
The script is register_bp.sh. then run following command. This command depends on fibos
```
fibos register_bp.js
```
The up command is depends on fibos. If your didn't install it run this:
```
curl -s https://fibos.io/download/installer.sh | sh
```
## Install and Start docker
Just run next command, your would start your bp, and it has been set up autorun if you reboot your computer.(All following code should run under docker-fibos-eosio-producer directory.)
```
sudo docker-compose up -d
```
If your want to stop your bp, run this:
```
sudo docker-compose stop
```
IF your want to start your bp, run this:
```
sudo docker-compose start
```
If your want to see pb log, run this:
```
sudo docker-compose logs
```
# How to upgrade?
Change current directory to git project dir, then run following code:
```
./upgrade.sh
```
# How to claim rewards?
Change current directory to git project dir, then run following code:
```
fibos earn_bp.js
```
# Finally
If you like my repo, your can run the following command and vote for me (williamfouvy).  Next command depends some programs: fibos, which I have describe in the section Register producer(optional)
```
fibos vote_william.js
```
Thank you.
