#!/bin/bash 

# GPU Info Check Command 
echo -e "\033[034m ############________GPU Info Check Command________##########"
sudo lshw -C display 

# Processor Info Check Command 
echo -e "\033[031m ##############_______Processor Info Check Command______########"
sudo dmidecode -t 4 | egrep -i 'core (count|enabled)|thread count|Version' 

# OS Info Check Command 
echo -e "\033[032m ##############_________OS Info Check Command_________###########"
cat /etc/os-release 


# Storage Info Check Command 
echo -e "\033[033m ###########_____________Storage Info Check Command_____________#############"
sudo /sbin/parted -l 

# Monitor Info Check Comamnd 
echo -e "\033[035m ###########_____________Monitor Info Check Comamnd_____________#############"
# hwinfo Install Command
sudo apt install hwinfo -y 
hwinfo --monitor 

# Ram Info Check Command 
echo -e "\033[036m ###########_____________Ram Info Check Command_____________#############"
sudo dmidecode --type 17 


# ram Speed Check Command 
echo -e "\033[037m ###########_____________ram Speed Check Command_____________#############"
sudo free -h 
sudo dmidecode -t memory | grep -i "speed" 

# Full_Info Check Command 
echo -e "\033[038m ###########_____________Full_Info Check Command_____________#############"
sudo apt install dmidecode 
sudo dmidecode 




