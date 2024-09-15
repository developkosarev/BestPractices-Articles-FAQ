Edit the New Relic Infrastructure configuration file:

```bash
sudo nano /etc/newrelic-infra.yml
```
Add or modify the following line to set a custom display name for the host:

```bash
display_name: "New_Host_Name"
```
Save the changes and restart the New Relic Infrastructure agent:

```bash
sudo systemctl restart newrelic-infra
```
