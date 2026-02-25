# Welcome to eve.js!
> [!WARNING]
> Right now, the only code published here is the code that completes the handshake, as that is the only code that is 100% completed and works.
> [!WARNING]
> This repository is in its very early stages, so do not expect everything to work perfectly. I am still learning to use JavaScript, so the code could be improved. Feel free to open a PR!

### Getting started (Part 1):
You will firstly need to patch the client. The eve.js server can only understand Placebo encoded packets, so you will need to change `start.ini` to be Placebo instead of CryptoAPI. The game will not start with a modified `start.ini` so we will have to replace `blue.dll` with a patched version.

**WARNING: It is strongly recommended to clone the Eve Online install files to a seperate directory before editing any files!**

* **Step 1:** Clone the Eve Online install to a seperate location
* **Step 2:** Download `blue_patched.dll` from [this Github release](https://github.com/evejs-emu/eve.js/releases/tag/blue.dll)
* **Step 3:** Rename `blue_patched.dll` to `blue.dll`
* **Step 4:** Move the file to the `bin64` folder inside the cloned Eve Online install directory
* **Step 5:** Click 'Replace the file in this destination' when prompted

Now that `blue.dll` has been replaced, we need to change `start.ini`. It will be located in the root directory of your cloned Eve Online directory.\
Open it in Notepad, then replace `CryptoAPI` with `Placebo`. Then replace `Tranquility` with `localhost`. Save the file, then you are done with part 1.

*(optional): if you want to avoid finding the specific exe file to launch every time, you can right click the `exefile.exe` inside the `bin64` direcotry, then click 'Show more options' (if on windows 11), then 'Send to' > 'Desktop (create shorcut)'*
