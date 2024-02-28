# Consequat Studio Common repository

## Common Repository setup

* Enable git symlinks

    ```sh
    git config core.symlinks true
    ```

* Add this repo as a submodule by running following command from a shell

    ```sh
    git submodule add https://github.com/consequat-studio/common.git sub/common
    ```

* Checkout organization specific branch

    ```sh
    cd ./sub/common
    git checkout org-specific
    cd ../..
    ```

* Create symbolic links for common files and copy license file by running shell script based on OS

    * *nix bash:
    ```sh
    ./sub/common/scripts/init.sh
    ```

    * Windows PowerShell (requires: GIT installed, administrator privileges):
    ```powershell
    Start-Process -verb RunAs "$env:PROGRAMFILES\Git\bin\sh.exe" "./sub/common/scripts/win-init.sh"
    ```


## Update Common Repository

* Run following commands from repository root

    ```sh
    git submodule update --remote ./sub/common
    ```
