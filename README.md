# Lovelace power usage graph card

This card will display a doughnut chard that represents your current power Usage. 

## Usage
1. Add plugin .js as a module:
```
- url: /local/lovelace-graph-card.js
  type: module
```
2. Add lovelace card to view:
```
- type: "custom:power-usage-card"                  # Mandatory
  title: "Actueel stroomverbruik"                  # Optional customized title
  total_power_usage: sensor.power_consumption      # Optional total power consumption (DSMR) sensor.
                                                   # If available then other measured values will be 
                                                   # substracted from total to calculate 'unknown' value.
  unknownText: "Onbekend"                          # Optional customized unknown text. Only applicable
                                                   # with total_power_usage option enabled.
  entities:
    - entity: sensor.dimmer_kitchen_power          # One or more entities providing Watt (W) measurements
      name: Keuken                                 # Optional customized name for entity
    - entity: sensor.dimmer_garage_power
      name: Garage
    - entity: sensor.wall_plug_livingroom_left
      name: Huiskamer links
    - entity: sensor.wall_plug_livingroom_tv
      name: Huiskamer TV
 ```

![screenshot](https://raw.githubusercontent.com/cheelio/power-usage-card/master/power-usage-card.png)
