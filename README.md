<img width="827" height="125" alt="image" src="https://github.com/user-attachments/assets/21a1a9c8-6006-4c8d-942c-c1454de7b347" /># Hackintosh EFI for 2015 Alienware Alpha
Hackintosh EFI using OpenCore Bootloader for Alienware Alpha. 
### How to setup
- Go to `releases/oc`, or simply go to the Releases tab in the bottom right.
  
  <img width="440" height="169" alt="image" src="https://github.com/user-attachments/assets/9daa19db-c16d-402d-b293-bc73f44cbcdc" />
- Grab a copy of the release .ZIP file, `OC1.0.5-EFI-AlienwareAlpha-IntelCorei3-UEFI-NTCBLS-Goggles.zip`.
- Unzip this file to get the folder EFI. 
- Format a USB Drive **with FAT32** (If over 64GB, use Rufus to make FAT32 formatted partition. See [Rufus.png](https://github.com/SaiPanneerselvam/Hackintosh-Alienware-Alpha/blob/main/resx/Image_RElease_Rufus.png?raw=true)).
**NOTE: When labeling the drive, choosing names that are small and don't contain spaces ensures compatibilty for booting MacOS**
- Copy "EFI" Folder to the drive.
#### 🎉 You have a bootable drive! 🎉
However, don't stop there, unless you are aware of what you are doing. Next:
- Download the tool "`macrecovery.py`" from OpenCorePkg [here](https://github.com/acidanthera/OpenCorePkg/blob/master/Utilities/macrecovery/macrecovery.py). This tool downloads MacOS recovery images, which is used to download and install MacOS
- Start a `CMD` instance at the location that you have macrecovery.py. 
<img width="1123" height="612" alt="image" src="https://github.com/user-attachments/assets/08f3e83f-cad9-43ac-baa1-0cf088c3ae37" />
- In this `CMD` instance, choose which version of MacOS you plan on using from this list:

```
# Lion (10.7):
py macrecovery.py -b Mac-2E6FAB96566FE58C -m 00000000000F25Y00 download
py macrecovery.py -b Mac-C3EC7CD22292981F -m 00000000000F0HM00 download

# Mountain Lion (10.8):
py macrecovery.py -b Mac-7DF2A3B5E5D671ED -m 00000000000F65100 download

# Mavericks (10.9):
py macrecovery.py -b Mac-F60DEB81FF30ACF6 -m 00000000000FNN100 download

# Yosemite (10.10):
py macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000GDVW00 download

# El Capitan (10.11):
py macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000GQRX00 download

# Sierra (10.12):
py macrecovery.py -b Mac-77F17D7DA9285301 -m 00000000000J0DX00 download

# High Sierra (10.13)
py macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000J80300 download
py macrecovery.py -b Mac-BE088AF8C5EB4FA2 -m 00000000000J80300 download

# Mojave (10.14)
py macrecovery.py -b Mac-7BA5B2DFE22DDD8C -m 00000000000KXPG00 download

# Catalina (10.15)
py macrecovery.py -b Mac-00BE6ED71E35EB86 -m 00000000000000000 download

# Big Sur (11)
py macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download

# Monterey (12)
py macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000000000 download

# Ventura (13)
py macrecovery.py -b Mac-4B682C642B45593E -m 00000000000000000 download

# Sonoma (14)
py macrecovery.py -b Mac-226CB3C6A851A671 -m 00000000000000000 download

# Latest version
# ie. Sequoia (15)
py macrecovery.py -b Mac-937A206F2EE63C01 -m 00000000000000000 download

```
- macrecovery.py will download an BaseSystem.dmg and BaseSystem.chunklist (for most models), in a folder named com.apple.recovery.boot .
- Move this folder to the USB Drive, to be alongside the EFI.
<img width="827" height="125" alt="image" src="https://github.com/user-attachments/assets/c612c114-5a63-4c9b-8071-380c3f375cdb" />


#### All you need to do is to simply boot the USB Drive on your Alienware Alpha
### 🎉 You are finished! 🎉

