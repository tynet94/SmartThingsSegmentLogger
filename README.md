# SmartThingsSegmentLogger

## Segment.com Setup
1. Get a Segment.com account
1. Create a new Segment.com source for your smartthings location (aka `MySmartThingsLocation`)
1. Get API Write Key from `Segment.com->Connections->Sources->MySmartThingsLocation->Settings->APIKey->WriteKey`
1. Base64 encode your Write Key appended with a colon (no newline)
```bash
echo -n 'someKey123abcXYZ:' | base64 '
c29tZUtleTEyM2FiY1hZWjo=
```
## SmartThings App in Developer Mode
1. Launch the SmartThings app
1. Go to the `Dashboard>Settings>About SmartThings`
1. Press `About SmartThings` for 5 seconds
1. Now press `Developer Mode`
1. Relaunch the SmartThings app making sure you are logged in

## Add Repo to SmartThings IDE
1. Go to IDE: `something.api.smartthings.com->MySmartApp->Settings`
1. Add Owner `tynet94` Name `SmartThingsSegmentLogger` Branch `main`
1. Hit `Save`

## Install Segment Event Logger into IDE
1. From IDE My SmartApp webpage, click `Update from Repo` and select the above repo
1. Select the files in the `New (only in Github)` section
1. Select the `publish` and hit `Execute Update` button at the bottom left

## Create SmartApp Instance
1. In SmartThings App automation tab, click `+` and `Add routine`
1. Click `Discover` tab and scroll to the bottom
1. Click `Segment Event Logger`
1. Add base64 encoded write key
1. Select the switches you'd like to log
1. Assign logger instance a name "MyLocation Production"
1. Enable for all modes
1. Hit `Done`
