# Unifi Network Application
This is the selfhosted version of the Unifi Console - Network Application. It allowes the management of unifi network devices.

## Trouble shouting
In case devices ar not found on the network to be adopted try these mehtods.

### Unifi App
The Unif App on a spartphone can discover devices ready for adoption and point them to the console that is active in the app.

1. Install the unifi app on a smart phone. 
0. Connect it to the same network as the to be adopted device
0. Add your selfhosted console (Network Application) to the Unifi App.
0. Navigate to the Unifi Devices tab.
0. After a few moments the device ready for adoption should show up.

### Unifi SSH
If the app does not help and it is an enterprise device the shell can configure the console address.

1. reset the device (otional if credentials are known)
0. connect to it via ssh (defaults : {user : ubnt, pass: ubnt})
0. once connected run the shell command 
   ```
   set-inform http://$address:8080/inform
   ```