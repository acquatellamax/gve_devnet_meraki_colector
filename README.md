# gve_devnet_meraki_colector
Python script that collects data from a Meraki API call and stores it in a .csv file.
This script will collect information for the following: 

Meraki MX interface status
Meraki MX loss and latency information

The script will bulk-collect this information every period of time (set in the script, ideally every 1+ minute)


## Contacts
* Max Acquatella

## Solution Components
* Meraki MX
* Python 

## Requirements
Cisco Meraki Administrator Token (can be obtained from the Meraki Dashboard)
See more here:

https://documentation.meraki.com/General_Administration/Other_Topics/Cisco_Meraki_Dashboard_API


## Installation/Configuration

Install python 3.6 or later

Add credentials to the credentials.py script

Set up and activate a virtual environment (https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)

```
python3 -m venv env
source env/bin/activate
```

Make sure to activate the virtual environment before proceeding to the next step


Install requirements.txt via command line

```
pip install -r requirements.txt
```

Main script: main_collector.py

The collector timer is set in lines 111 and 112 of main_collector.py (set to 1.05 min).
This can be changed to values greater than one min.
NOTE: the meraki API will not show information for less than one min.

![/IMAGES/image2.png](/IMAGES/image2.png)


## Usage

Run main_collector.py from your command line:

```
python3 main_collector.py
```

The code should generate two .csv files (response1.csv and response2.cvs) in the same project folder. 
The files will contain information similar to this:

# Screenshots

![/IMAGES/image1.png](/IMAGES/image1.png)

### LICENSE

Provided under Cisco Sample Code License, for details see [LICENSE](LICENSE.md)

### CODE_OF_CONDUCT

Our code of conduct is available [here](CODE_OF_CONDUCT.md)

### CONTRIBUTING

See our contributing guidelines [here](CONTRIBUTING.md)

#### DISCLAIMER:
<b>Please note:</b> This script is meant for demo purposes only. All tools/ scripts in this repo are released for use "AS IS" without any warranties of any kind, including, but not limited to their installation, use, or performance. Any use of these scripts and tools is at your own risk. There is no guarantee that they have been through thorough testing in a comparable environment and we are not responsible for any damage or data loss incurred with their use.
You are responsible for reviewing and testing any scripts you run thoroughly before use in any non-testing environment.