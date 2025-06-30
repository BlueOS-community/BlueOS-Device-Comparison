# Doppler Velocity Loggers (DVLs)

- [Device type description](https://docs.bluerobotics.com/ardusub-zola/hardware/additional/positioning-sensors/#dvl-positioning-systems)
- [Technology description](https://bluerobotics.com/learn/a-smooth-operators-guide-to-underwater-sonars-and-acoustic-devices/#doppler-velocity-logger)

## Relevance to BlueOS

Position estimates are important for position holding, path following, and vehicle autonomy. DVLs are a common source of positioning information (via velocity integration) for underwater vehicles, and often don't have direct integration with flight controller autopilot firmwares, so BlueOS is a useful compatibility layer.

# Comparison

|Manufacturer|Model|Cost (USD)|Alternative Source(s)|BlueOS Integration?|Depth rating (m)|Min. altitude (m)|Max.<sup>1</sup> altitude (m)|Max. speed (m/s)|Long Term Accuracy|Diameter (mm)|Height (mm)|Mass (kg)|Volume (L)|Avg. Power (W)|DC input (V)|Freq. (kHz)|Ping rate (Hz)|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Cerulean|[DVL-75 (OEM)](https://ceruleansonar.com/products/dvl-75-oem)|**$2,299-$2,943**|?|[Extension](https://docs.bluerobotics.com/BlueOS-Extensions-Repository/#:~:text=Cerulean%20DVL,-Maintainer)|300|0.3|40+|4.12|?<sup>2</sup>|77|33|**0.25**|0.1 (+elec)|8|12-24|675|5-20
|Cerulean|[DVL-75 most-/<br>all-in-one](https://ceruleansonar.com/products/dvl-75-with-housing-and-integrated-sensor-head)|$2,598-$3,641|?|[Extension](https://docs.bluerobotics.com/BlueOS-Extensions-Repository/#:~:text=Cerulean%20DVL,-Maintainer)|300|0.3|40+|4.12|?<sup>2</sup>|82|111|0.73|0.52|8|12-24|675|5-20
|Water Linked|[A50<br>standard](https://waterlinked.com/shop/dvl-a50-114#attr=8,53)|$6,900/<br>$9,900|[BR Reef](https://bluerobotics.com/store/the-reef/dvl-a50/)|[Extension](https://docs.bluerobotics.com/BlueOS-Extensions-Repository/#:~:text=Water%20Linked%20DVL,-Maintainer)|300/<br>**600**|**0.05**|50|3.75|1.01%|**66**|**25**|**0.25**|**0.1**|**3**|10-30|1000|4-26
|Water Linked|[A50<br>performance](https://store.waterlinked.com/product/dvl-a50/)|$7,880/<br>10,880|?|[Extension](https://docs.bluerobotics.com/BlueOS-Extensions-Repository/#:~:text=Water%20Linked%20DVL,-Maintainer)|300/<br>**600**|**0.05**|50|3.75|**0.1%**<sup>3</sup>|**66**|**25**|**0.25**|**0.1**|**3**|10-30|1000|4-26
|Teledyne|[Wayfinder](http://www.teledynemarine.com/Wayfinder)|$7,500|?|(Companion) [Guide](https://discuss.bluerobotics.com/t/dvl-recommendations/10775/4) |200|0.5|60|**10**|1.15%|100x100sq|70|0.85|0.7|**3**|11.4-36.7|600|<=16
|Nortek|[Nucleus1000](https://www.nortekgroup.com/products/nucleus1000)|<$10,000/<br>?|?|[Extension](https://docs.bluerobotics.com/BlueOS-Extensions-Repository/#:~:text=Nortek%20Nucleus,-Maintainer)|300/<br>1000|0.1|50|?|1.01%/ 0.3%<sup>3</sup>|90|42|0.535||<4|10-32|1000|<=8

<sup>1</sup> Achieved maximum altitude in a given scenario depends on factors such as tilt of the sensor head; flatness, hardness, and vegetation cover of the bottom; and salinity.

<sup>2</sup> Cerulean provides "median expected dead reckoning circular error" (which the others don't provide) as 5% of distance travelled. They don't provide a long term velocity accuracy, so probably those numbers aren't comparable.

<sup>3</sup> Export controlled.

> ***NOTE:** If anyone is interested in comparing **more options** and/or **extra details**, there's a [**public spreadsheet**](https://docs.google.com/spreadsheets/d/1OgTeGA1q29m4dUGCgHnPJI83A21Asu1V5mgdpjjWHt8/edit?usp=sharing) - feel free to add more information on any DVL options that are suitable for inspection-class ROVs. There are already a few in there beyond what the table here includes :-)
