# findItems

FindItems is a Python script that queries information from an ArcGIS Portal and consolidates it into a spreadsheet.

Please note that you should be using Python 3.7.6 for the ArcGIS Library to work. Additionally, you would need to do the same with any instances where you want to use the ArcGIS Library.

### Please skip the first part of the install guide if you are running Windows and just install the necessary modules by running:

    pip install -r .\requirements.txt

## Installation

To use FindItems, you need to install the following Linux library:

    sudo apt-get install libkrb5-dev

You will also need to install the Rust programming language by running the following command:

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

Then, add Rust to your environmental variables by running:

    source "$HOME/.cargo/env"

After installing the necessary Linux library, install the required Python modules by running:

    pip install --upgrade sip
    pip install -r .\requirements.txt


## Usage

To use findItems, run the script once. This will generate a config.ini file. Next, fill in your relevant Portal credentials within the config.ini file. Finally, run the script again to start using findItems.

findItems will query the information on the portal, such as:

- Portal item ID
- Portal Content name
- Portal Content Owner
- Portal Item Size

It will then consolidate all that information into a spreadsheet.
Please note that it will skip owners: esri_nav, esri_apps and esri.
