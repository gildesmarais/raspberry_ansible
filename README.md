# Bodos Raspberry PI

This is the configuration for my Raspberry PI.

Steps to install it on your machine:

* Install [NOOBS](https://github.com/procount/noobsconfig/) on the Raspberry
* Select the non ui version of raspbian
* Wait till it is installed and login using `pi` and `raspberry` as password
* Activate ssh as described [here](https://www.raspberrypi.org/documentation/remote-access/ssh/README.md).
* Add your ssh key to the `.ssh/autorized_keys` file on the Raspberry
* Change the IP in the [`hosts`](hosts) file to the IP of your Raspberry
* Install ansible with `brew install ansible`
* `sh run.sh`
* Now you have [InfluxDB](https://docs.influxdata.com/influxdb) and [Grafana](http://grafana.org/) installed on the machine
* Open `http://[yourip]:3000` to see the Grafana interface and go through the
  wizard to configure the database connection (the InfluxDB password can be
  found in the `playbook.yml`)

And now you need some data to put into your influxdb to make it
worth it. For example you could build a small air pollution sensor for around
30€ that pushes data into it. Details can be found [here](http://luftdaten.info/).
