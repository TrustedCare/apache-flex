# Apache-FLEX
---
Installs or updates Apache Flex using ANT.

Following the instructions for building Flex using the [Apache README](https://dist.apache.org/repos/dist/release/flex/installer/3.2/READme).  At the time of this writing, the instructions are as follows:

```
==========================================================================================
How to build the installer using ANT (no Flash Builder or any other IDE required):
==========================================================================================

0.  Make sure you have the right version of the Adobe AIR SDK.  Apache Flex Installer
    3.1 uses Adobe AIR SDK 4.0.  If you want to use an older version of the AIR SDK,
    you will have to change the namespace in the following files:
	installer/src/InstallApacheFlex-app.xml
	ant_on_air/tests/AntOnAIR-app.xml.

1.  Unzip the source distribution.  You should see the 'installer' directory and the
    'common' and 'ant_on_air' directories in the root.

2.  In the ant_on_air directory, run:
        ant [-DFLEX_HOME=/path/to/apache/flex/sdk] [-DAIR_HOME=/path/to/air/sdk]

    FLEX_HOME is the absolute path to the Apache Flex SDK
        If you omit this argument, and the system environment variable, FLEX_HOME exists,
        it is used.  Otherwise, the FLEX_HOME_MAC or FLEX_HOME_WIN property in
        installer/build.properties is used.

    AIR_HOME is the absolute path to the Adobe AIR SDK
        If you omit this argument, and the system environment variable, AIR_HOME exists,
        it is used.  Otherwise, the AIR_HOME_MAC or AIR_HOME_WIN property in
        installer/build.properties is used.

3.  In the installer directory, run:
        ant build [-DFLEX_HOME=/path/to/apache/flex/sdk] [-DAIR_HOME=/path/to/air/sdk]

4.  The installer executable file created in the installer/release directory.  If you are
    on Windows, you will see an .exe file; if you are on Mac OS, you will see a .dmg file.  
	A temporary digital signing certificate - temp.p12 will be created in the installer
	directory as well.  The password for this file is available in the build.properties
	file (var: TEMP_PASS_CHANGE_THIS)
  ```

## Requirements
---
Assumes that ANT is already installed.

## Role Variables
---
* `flex-installer-url`: Specifies the URL to download the flex sdk installer.
* `passenger_pkgs_state`: Specifies if this role will garantee that the packages are installed or installed and updated. Possible values: `installed` and `latest`. Defaults to `installed`.

## License
---
MIT

## Author Information
---
[GitHub project page](https://github.com/TrustedCare/apache-flex.git)
