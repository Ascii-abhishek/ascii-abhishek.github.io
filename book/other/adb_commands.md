# ADB (Android Debug Bridge) Commands

---

|Commands| Description |
|---|---|
|`adb tcpip 5555`<br> `adb connect device_ip_address` <br> `adb connect host:port` # if port not given then default port is 5555|To connect a device over wifi <br> # connect device via usb and enter first command, after that disconnect device and enter second command in terminal|
|`adb kill-server`| Reset adb host |
|`adb start-server`|Restart adb server and daemon after above command|
|`adb forward tcp:6100 tcp:7100` <br> `adb forward tcp:6100 local:logd`|Set up arbitrary port forwarding, which forwards requests on a specific host port to a different port on a device|
|`Adb devices -l`| List of attached devices in detail |
|`Adb install [option] path_to_apk` |Install an app into device <br>Options:<br> `-l`: forward lock app <br>`-r`: raplace existing package <br>`-t`: allow test packages <br>`-s`: install on sd card <br>`-d`: allow version code downgrade <br>`-g`: grant all runtime permissions|
|`adb uninstall [-k] package`|Reamove app, -k option is to keep the data and cache directories|
|`adb pull remote local`|copy data from device to host machine|
|`adb push local remote`|Copy data from host machine to device|
|`emulator -avd emulator_name -port 5555`|connect a pre-made emulator to port 5555|
|`adb -s device_adb_code command`|execute command on a specific device if multiple are connected|
|`adb -d command` # device <br> `adb -e command` # emulator|if device and emulator both are connected|
|`adb backup [option] package_name` |Backup phone apps data into PC <br>Options:<br>1. `-f file_name`: if file_name not given then backup.adb <br>2. `-apk / -noapk`: backup apk file also, default is -noapk <br>3. `-obb / -noobb`: backup obb file or not, -noobb is default <br>4. `-shared / -noshared`: backup shared storage or not <br>5. `-all`: backup app apps, package_name not required <br>6. `-system / -nosystem`: default is -system|
|`adb restore file_name`|restore data from backed up data file|
|`adb bugreport path`|Default filename is bugreport.zip, devices that do not support zipped bug reports print to stdout|
|`adb logcat [-help] [-option] [filter-spec]`||
|`adb reboot [bootloader / recovery / sideload / sideload-auto-reboot]`|Reboot device in specified mode|
|`adb get-serialno`|Print the adb device serial number string|
|`adb shell`|Start a remote interactive shell in the target device|
|`adb shell am [command]` |Activity Manager<br>Options:<br>1.  `start -a intent`: Start an activity specified by intent <br> #`adb shell am start -a android.intent.action.VIEW` <br> 2. `startservice [option] intent`: start a service specified by an intent <br>3. `force-stop package`: force stop everything associated with package <br>4. `kill-all`: kill all background processes <br>5. `profile start process file`: start profiler on process, write result to file <br>6. `profile stop process`: stop profiler on process <br>7. `display-size [reset / w*h]`: override display size <br> 8. `display-density new_dpi`: override display density|
|`adb shell dpm command`|device policy manager|
|`adb shell screencap /sdcard/screen.png`|Take a screenshot of device display|
|`adb shell screenrecord [option] /sdcard/demo.mp4`|Stop the screen recording by pressing Control + C; otherwise, the recording stops automatically at three minutes or the time limit set by --time-limit<br>Options: <br>`--help`: Help <br>`--size w*h`: default is 1280*720 if supported by device <br>`--bit-rate rate`: in megabits per second (4Mbps -> enter value 4000000) <br>`--time-limit time`: time limit in seconds. default is 180 <br>`--verbose`: display log information|
|`adb shell dmesg`|Print kernel debugging message to screen|
|`adb shell sqlite3 /path_in_device/file_name.db`|start sqlite3 command line program|

---

### `adb shell pm [command]`: Package Manager

|Commands| Description |
|--------|-------------|
|`list packages [option] filter` |Prints all packages, optionally only those whose package name contains the text in filter<br>Options:<br> `-f`: see their associated files <br>`-d`: filter to only show disabled packages <br>`-e`: show enabled packages <br> `-s`: show system packages <br> `-3`: show third party packages <br> `-i`: see the installer for the packages <br> `-u`: include uninstalled packages <br> `--user uid`: user space to query|
|`list permission-groups`|print all known permission groups|
|`list permission [option] group`|Print all known permissions, optionally only those in groups<br>Options: <br> `-g`: organized by group <br> `-f`: print all information <br>`-s`: short summary <br>`-d`: list dangerous permissions <br>`-u`: list only the permissions users will see|
|`list features`|Print all features|
|`list libraries`|Libraries supported by current device|
|`list users`|all users on the system|
|`path package`|Path to apk of the given package|
|`clear package`|delete all data associated to package|
|`grant package permission`|Grant a permission to an app|
|`revoke package permission`|Revoke a permission from an app|
|`set-install location location`|Change the default install location<br>Options: <br> 0: auto, let the system decide <br>1: internal <br> 2: external|
|`get-install-location`|return current default install location|
|`create-user user_name`|Create new user # supported in multi-user devices only|
|`remove-user uid`|Remove user with given user_id and data associated with them|
|`get-max-users`|Remove user with given user_id and data associated with them|
