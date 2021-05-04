# Config Snap

This is a snap that is used to configure Ubuntu Core based systems. It allows you to create;
* An extra-user which does not have "root" (sudo) priviledge
* A default network configuration.

## Build
Clone the repo and run the following command.
```
snapcraft --use-lxd
```

## Installation
You can install the snap package that you built with
```
snap install config-snap --dangerous
```

Please do not forget to add required plugs in your gadget snap file beforehand. Otherwise, config-snap will not work!


## Configuration
Initial configuration could be done by tweaking the `connect-plug-account-control` and `connect-plug-network-setup-control`  

```
snap set config-snap config="content of your netplan.yaml file"
```

Hint: You could use;
```sh
yournetplanyaml=`cat <pathofyourfile>`
snap set config-snap config="$cmd $yournetplanyaml"
```


## Enjoy

and provide feedback ;)