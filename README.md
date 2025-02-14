# Manage_Hyperthreading.sh

Manage_Hyperthreading.sh is a simple script to manage the Intel Hyper-Thread technology on some Intel CPUs.

This script parses both information in /sys/devices/system/cpu and lscpu to determine which cores are hyperthreaded, and to online or offline them.

This script works with certain* Google Compute Engine instances, and should work with most other cloud providers and other Intel Hyper-Thread enabled systems.
This script works on OCI's E4 and X9 instances. The script is being modified to add options.

You must run this script as root, and the script will not run if not run as root or under sudo.

\* NOTE: This script is not supported at all. It is not official Google code. Only select Google Compute Engine instances support disabling hyper-threads as of Jan 1, 2019. These are: n1-ultramem, and C2 instances.

Usage
-----
```
./manage_hyperthreading.sh [OPTIONS]
	OPTIONS
	-d | --disable		Disable Hyper-Threaded vCPUs
	-e | --enable		Enable Hyper-Threaded vCPUs
	-s | --show		Show Hyper-Threading status
	-h | --help		Display this usage output
```
