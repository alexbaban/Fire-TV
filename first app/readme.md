# First Fire TV App (install and run)

### Install the 'Web App Tester' App

You can install the 'Web App Tester' app from the 'Amazon Appstore' app on Fire TV device, 
or download it from the Amazon website (https://www.amazon.com/Amazon-Digital-Services-Inc-Tester/dp/B00DZ3I1W8).

### Download the 'Web App Starter Kit for Fire TV' from GitHub 

(https://github.com/amzn/web-app-starter-kit-for-fire-tv)

### Extract the 'simple' folder

From `\web-app-starter-kit-for-fire-tv-master\out\simple` directory to `C:\FireTVApps\simple` directory

### Create .zip for 'simple' (simple.zip)

- Enter the `C:\FireTVApps\simple` directory, then select all files and folders   
- Right click, then '7-Zip', then 'Add to "simple.zip"'

### Copy 'simple.zip' to device

- Connect the Fire TV device to computer
- Explore to `/sdcard/amazonwebapps` directory on the host device
- Copy 'simple.zip' from `C:\FireTVApps\simple\simple.zip` to `/sdcard/amazonwebapps/simple.zip`

### Launch the app with the 'Web App Tester' App

- Connect the Fire TV device to TV and turn on
- Launch the 'Web App Tester' app on Fire TV
- Select 'Test Packaged App' from the menu at the top right
- The 'simple.zip' should show under 'Apps on this device' section
- Select, then Verify, then Test

> Note: 'simple.zip' uploaded to this folder
