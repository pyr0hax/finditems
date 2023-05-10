# findItems

FindItems is a Python script that queries information from an ArcGIS Portal and consolidates it into a spreadsheet.

Please note that you should be using Python 3.9.16 for the ArcGIS Library to work. Additionally, you would need to do the same with any instances where you want to use the ArcGIS Library.

### Please skip the first part of the install guide if you are running Windows and just install the necessary modules by running:

    pip install arcgis
    pip install openpyxl

## Installation

To use FindItems, you need to install the following Linux library:

    sudo apt-get install libkrb5-dev

If there are complaints about the absence of Rust, you should install the Rust programming language by executing the provided command:

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

Then, add Rust to your environmental variables by running:

    source "$HOME/.cargo/env"

After installing the necessary Linux library, install the required Python modules by running:

    pip install --upgrade sip
    pip install arcgis
    pip install openpyxl



## Usage

To use findItems, run the script once. This will generate a config.ini file. Next, fill in your relevant Portal credentials within the config.ini file. Finally, run the script again to start using findItems.

findItems will query the information on the portal, such as:

- Portal item ID
- Portal Content name
- Portal Content Owner
- Portal Item Size

It will then consolidate all that information into a spreadsheet.
Please note that it will skip owners: esri_nav, esri_apps and esri.
