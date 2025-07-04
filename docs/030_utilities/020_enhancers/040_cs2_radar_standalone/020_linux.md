# Install on Linux (e.g. WSL)
The standalone radar is available for Linux systems and is designed to run in a virtual machine (VM) hosted on Windows using Zenith.

:::warning
Valthrun only supports Counter-Strike 2 on Windows.
Running the radar on Linux is intended solely for use with Zenith in a VM!
:::

## TL;DR Installation Steps
1. Open CMD (on Windows):  
   Launch Command Prompt from the Start Menu.

2. Install WSL:  
   ```bash
   wsl --install
   ```

3. Close CMD.  

4. Download Required Binaries:  
   - [Download driver interface (Linux)](https://valth.run/portal/artifacts/driver-interface-zenith/release-linux)
   - [Download radar client (Linux)](https://valth.run/portal/artifacts/cs2-radar-client/release-linux)

5. Open WSL.  
6. Move and Rename Binaries:  
   Replace `<username>` with your actual Windows username and `[...]` with the correct version hash from the filenames.

   ```bash
   mv /mnt/c/Users/<username>/Downloads/driver_interface_zenith_[...].so libdriver.so
   mv /mnt/c/Users/<username>/Downloads/cs2_radar_client_[...].so radar
   ```

7. Run the Radar:
   ```bash
   ./radar
   ```

## Installation
### 1. Enable and Install WSL on Windows

1. Open Command Prompt as Administrator.
2. Run the following command to install WSL and the default Ubuntu distro:

   ```bash
   wsl --install
   ```

3. Reboot your machine if prompted.

4. Once rebooted, allow Ubuntu (or your chosen distro) to finish setting up. You will be prompted to create a **Linux username and password**—choose anything you like.

### 2. Download Required Radar Files
1. Open a browser on Windows and download the following two files:
   - **Driver Interface (Zenith)**  
     [Download driver_interface_zenith](https://valth.run/portal/artifacts/driver-interface-zenith/release-linux)
   - **Radar Client**  
     [Download cs2_radar_client](https://valth.run/portal/artifacts/cs2-radar-client/release-linux)

2. These will be saved in your default Windows Downloads folder, e.g.,  
   `C:\Users\<YourUsername>\Downloads\`

### 3. Move and Rename Files in WSL

1. Open WSL (Ubuntu) via the Start Menu or terminal.

2. Move and rename the downloaded files from the Windows filesystem into your Linux environment.

   Replace `<YourUsername>` with your actual Windows username, and update the filenames to match the version you downloaded (e.g., `driver_interface_zenith_ab12cd34ef.so`):

   ```bash
   mv /mnt/c/Users/<YourUsername>/Downloads/driver_interface_zenith_*.so libdriver.so
   mv /mnt/c/Users/<YourUsername>/Downloads/cs2_radar_client_*.so radar
   ```

   :::info
   The `/mnt/c/...` path gives WSL access to your Windows C: drive.
   :::

### 4. Run the Radar

Finally, launch the radar client:

```bash
./radar
```

If everything is set up correctly, you should see the following message:  
  
![image](@site/docs/_media/screenshot_standalone_web_radar_started.png)