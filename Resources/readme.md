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