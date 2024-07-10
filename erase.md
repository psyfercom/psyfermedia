Here are the detailed instructions, including how to run Terminal as an admin on Windows and uninstall Rust:

### For Windows:

#### 1. Uninstall WSL and Ubuntu:
1. Press **Windows + X** on your keyboard.
2. Select **Windows Terminal (Admin)** from the menu.
3. In the terminal, type the following commands and press Enter after each:
   ```sh
   wsl --unregister Ubuntu
   wsl --uninstall
   ```

#### 2. Uninstall Programs:
1. Press **Windows + I** on your keyboard to open **Settings**.
2. Click on **Apps**.
3. Scroll through the list of installed apps to find and uninstall:
   - Rust
   - Visual Studio Code
   - Git
4. Click on each app and select **Uninstall**. Follow the prompts to complete the uninstallation.

#### 3. Uninstall Rust:
1. Press **Windows + X** on your keyboard.
2. Select **Windows Terminal (Admin)**.
3. In the terminal, type the following command and press Enter:
   ```sh
   rustup self uninstall
   ```
4. Follow the prompts to confirm the uninstallation.

#### 4. Delete Project Files:
1. Open **File Explorer** by pressing **Windows + E** on your keyboard.
2. Navigate to the location where the `Argochain` folder is stored. This is usually in `Documents` or `Downloads`.
3. Right-click on the `Argochain` folder and select **Delete**.

### For macOS:

#### 1. Uninstall Programs:
1. Open **Finder**.
2. Go to the **Applications** folder.
3. Find and drag the following applications to the **Trash**:
   - Rust
   - Visual Studio Code
   - Git

#### 2. Uninstall Rust:
1. Open **Terminal**.
2. Type the following command and press Enter:
   ```sh
   rustup self uninstall
   ```
3. Follow the prompts to confirm the uninstallation.

#### 3. Delete Project Files:
1. Open **Finder**.
2. Navigate to the location where the `Argochain` folder is stored. This is usually in `Documents` or `Downloads`.
3. Right-click on the `Argochain` folder and select **Move to Trash**.

### For Linux (Ubuntu):

#### 1. Uninstall Programs:
1. Open the **Terminal** by pressing **Ctrl + Alt + T** on your keyboard.
2. Type the following commands and press Enter after each:
   ```sh
   sudo apt-get remove rustc cargo git clang curl libssl-dev llvm libudev-dev make protobuf-compiler
   sudo apt-get autoremove
   ```

#### 2. Uninstall Rust:
1. In the terminal, type the following command and press Enter:
   ```sh
   rustup self uninstall
   ```
2. Follow the prompts to confirm the uninstallation.

#### 3. Delete Project Files:
1. In the terminal, type the following command and press Enter:
   ```sh
   rm -rf ~/Argochain
   ```

### Removing Environment Variables:

#### Windows:
1. Press **Windows + R** to open the Run dialog.
2. Type `sysdm.cpl` and press Enter.
3. In the System Properties window, click the **Advanced** tab.
4. Click **Environment Variables**.
5. In the Environment Variables window, look for entries related to Rust or other setup tools.
6. Select the entry and click **Delete**.

#### macOS and Linux:
1. Open the **Terminal**.
2. Open your shell profile for editing:
   - For macOS and Linux, this might be `~/.bash_profile`, `~/.zshrc`, or `~/.bashrc`.
3. Type the following command and press Enter (replace `~/.bashrc` with the appropriate file if different):
   ```sh
   nano ~/.bashrc
   ```
4. Look for lines related to Rust or other setup tools and delete them.
5. Press **Ctrl + X**, then **Y**, and then **Enter** to save and exit the editor.
6. Reload the profile by typing:
   ```sh
   source ~/.bashrc
   ```

These detailed steps should help ensure that only the files and software related to the Substrate node setup are removed while keeping the rest of the system intact.
