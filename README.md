# moco-cli
<img src='https://img.shields.io/github/languages/code-size/Besnn/moco-cli?style=plastic'></img> 
<img src='https://img.shields.io/github/license/Besnn/moco-cli?color=blue&style=plastic'></img>  
**Mo**ney **Co**nverter on the CLI

## Features
<ul>
    <li>Quick and Simple</li>  
    <li>Standalone (only <em>bash</em> and <em>bc</em>)</li>  
    <li>Supports 166 currencies and cryptocurrencies</li>
</ul>

## Installation
Clone repository  
    ```
    git clone https://github.com/Besnn/moco-cli
    ```  

Add user permission with `sudo chmod u+x moco-cli/moco`  


When you type `ls && ls moco-cli` you should have something like this:  
![ls && ls moco-cli](/assets/ls.png)

### Setting PATH
#### Linux
Open you `.bashrc` now: `nano ~/.bashrc`  


Add `export PATH=<absolute_directory_of_script>:$PATH` (no angle brackets)

You can get the absolute path with `realpath <directory>/moco-cli`  
If that doesn't work try `echo $(pwd)` while inside `moco-cli`.

Finally, type `source ~/.bashrc`.  

#### MacOS
Open your `paths` file with `nano /etc/paths`.  

Add there the full path of the script.

## Usage
![usage0](/assets/usage0.gif)  
Syntax is: `moco <amount> <from_currency> <to_currency> [<to_currency>]`  
You can set an alias for `moco` by adding `alias <alias>="moco"` in your `.bashrc`.

The script can accommodate a maximum of one extra to-currency as that is the limit of the free API version.  

If you encounter any problems, make sure to get [your own API key](https://free.currencyconverterapi.com/)   
and put it in the `API_KEY` variable in the beginning of the script.  

Type `moco help`, `moco -h`, `moco -l` or similarly to list supported currencies.

If you cannot remember the trigram for your currency, use either `moco find <currency>` or `moco give <currency>`:
```shell
moco give dollar
# or you can use the | (or) operator (provided it's within quotes)
moco find "euro|lira|peso"
moco give 'lir|phil' # supports partial names
```
Make sure to change `MOCO_DIR` variable inside script in order for the above functionalities to work.
