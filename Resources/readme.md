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