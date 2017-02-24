# oracledb-ansible
This essentially is a fork of [cvezalis/oracledb-ansible](https://github.com/cvezalis/oracledb-ansible) with some minor
personal tweaks.

Could not get the full installation to run by now due to the following errors:
* Bug in Vagrant 1.9 that fails to assign static IP on CentOS
* Creating the databases with `dbca` exits with `TNS:… Listener lost contact`

Would be glad anyone can fix the second issue, it also occurs with a manually assigned static IP.
