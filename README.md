# MalLoader
A Python script designed to run malware nearly undetected (trojan horse), disguised by a simple survival text game. Detected by 1/65 vendors (DeepInstinct) on VirusTotal with full payload.

# DISCLAIMER
*FOR EDUCATIONAL USE ONLY. ONLY USE ON YOUR OWN PERSONAL DEVICES. I AM NOT LIABLE FOR ANY DAMAGES OR ACTIONS CAUSED BY THIS SCRIPT. BY DOWNLOADING AND USING THIS REPOSITORY YOU TAKE FULL RESPONSIBILITY FOR ANY ACTIONS COMMITTED*

# Requirements:
-Pyinstaller (to compile scripts)

-Python 3.10 or higher

-My block encryption program

-An example payload (restarts your computer) and blank key file are included to help with understanding the file layout.

# Steps
1. Download this repository
2. Download the block encryption repository
3. Write/place malware script into 'Data' folder, named as CharacterSet.py. Any functions within your script must be placed inside in "def main():" with no call to main().
4. Copy ANY used imports from your script into the top of HelperModule.py. Failure to do this may generate "Failure to import" errors at runtime.
5. Rename CharacterSet.py to CharacterSet.txt
6. Use block encryption to generate a private key
7. Place private key labeled as "WeightedValues.txt" into the "Data" folder
8. Use the block encryption program (level 3) to encrypt CharacterSet.txt
9. Use Pyinstaller to compile Game.py and HelperModule.py
10. Place all files generated in the respective 'dist' folders into the same directory as the respective python files
11. Delete Game.py, HelperModule.py, and any folders generated by Pyinstaller during compilation
12. Run 'Game.exe'
