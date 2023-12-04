# ArduninoEspressif32 ETH library example

```
ETH.begin(
        (uint8_t)      phy_addr,       # 1
        (int)             power,       # 5
        (int)               mdc,       # 23
        (int)              mdio,       # 18
        (eth_phy_type_t)   type,       # ETH_PHY_LAN8720
        (eth_clock_mode_t) clock_mode  # ETH_CLOCK_GPIO17_OUT
        );
```

|GPIO|USED BY|COMMENTS|
|----|-------|--------|
|GPIO5|Power on/off|Active High signal to power on the LAN7820 IC
|GPIO17|RMII Clock 50 MHz|Clock sourced from ESP32 APLL
|GPIO18|PHY MDIO||
|GPIO19|ETH TXD0||
|GPIO21|ETH TX_EN||
|GPIO22|ETH TXD1|
|GPIO23|PHY MDC||
|GPIO25|ETH RXD0||
|GPIO26|ETH RXD1||
|GPIO27|ETH CRS_DV||

## ESPhome example
```
esphome:
  name: esp32-ethernet
  friendly_name: esp32-ethernet

esp32:
  board: esp32dev
  framework:
    type: arduino

# Enable logging
logger:

# Enable Home Assistant API
api:
  encryption:
    key:

ota:
  password:

ethernet:
  type: LAN8720
  mdc_pin: GPIO23
  mdio_pin: GPIO18
  clk_mode: GPIO17_OUT
  phy_addr: 1
  power_pin: GPIO5

  # Optional manual IP
  # manual_ip:
  #   static_ip: 192.168.0.100
  #   gateway: 192.168.0.1
  #   subnet: 255.255.255.0
```
