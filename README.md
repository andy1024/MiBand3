**Work in progress**

# Xiaomi MiBand
Library to work with Xiaomi MiBand 2/3 (Supports python3)
[Read the Article here](https://medium.com/@a.nikishaev/how-i-hacked-xiaomi-miband-2-to-control-it-from-linux-a5bd2f36d3ad)

# Contributors & Info Sources
1) Base lib provided by [Leo Soares](https://github.com/leojrfs/miband2)
2) Further updates by [Volodymyr Shymanskyy](https://github.com/vshymanskyy/miband2-python-test), [Mathieu Jobin](https://github.com/mathieujobin/MiBand3)
3) Some info that really helped taken from [Freeyourgadget team](https://github.com/Freeyourgadget/Gadgetbridge/tree/master/app/src/main/java/nodomain/freeyourgadget/gadgetbridge/service/devices/huami/miband2)
4) code updated to work with python3/new bluepy

# Run

1) Install dependencies
```sh
pip install -r requirements.txt
```
2) Turn on your Bluetooth
3) Unpair you MiBand from current mobile apps
4) Find out you MiBand MAC address
```sh
sudo hcitool lescan
```
5) Run this to auth device
```sh
python main.py MAC_ADDRESS --init
```
6) If you having problems(BLE can glitch sometimes) try this and repeat from 4)
```sh
sudo hciconfig hci0 reset
```
7) Use the band with minimalistic UI by issuing (without parameters)
```sh
python main.py MAC_ADDRESS
```

### If you have trouble installing bluepy

```sudo apt-get install libglib2-dev  ```

