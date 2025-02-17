# Meshview

This project watches a MQTT topic for meshtastic messages, imports them to a
database and has a web UI to view them.
Requires Python 3.12

## Preparing

Clone the repo from github with:
``` bash 
git clone --recurse-submodules https://github.com/pablorevilla-meshtastic/meshview.git
```
> [!NOTE]
> It is important to include the `--recurse-submodules` flag or the meshtastic protobufs won't be included.

Create a python virtual environment:
``` bash
cd meshview
python3 -m venv env
```
Install the environment requirements:
``` bash
./env/bin/pip install -r requirements.txt
```
You also need to install `graphviz`:
``` bash
sudo apt-get install graphviz
```
Edit `config.ini` to change the MQTT server and topic

Other Options:
* `port`

   Web server port, default is `8081`

## Running Meshview

``` bash
./env/bin/python main.py
```
Now you can hit http://localhost/
