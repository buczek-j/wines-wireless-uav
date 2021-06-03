# wines-wireless-uav
Public Repo for Publication "What is A Wireless UAV?A Design Blueprint for 6G Flying Wireless Nodes"

![](https://github.com/buczek-j/wines-wireless-uav/blob/main/doc/monarch.jpg)

## Setup 
### UAV Parts list

The list of the off-the-shelf components used in the design of our UAV include:

* [Motors: T-Motor MN501-S KV240](https://store-en.tmotor.com/goods.php?id=695)
* [Propellers: T-Motor G20x6.5](https://store-en.tmotor.com/goods.php?id=496)
* [ESCs: T-Motor FLAME 60A 12S ](https://store-en.tmotor.com/goods.php?id=370)
* [Frame: Iflight iXC15 950mm](https://shop.iflight-rc.com/index.php?route=product/product&path=25&product_id=695)
* [Flight Controller: Holybro Pixhawk Mini](http://www.holybro.com/product/pixhawk-mini/)
* [Batteries: 4S 6000mAh (2 in series for 8s)](https://www.amazon.com/HOOVO-Connector-Airplane-Helicopter-Quadcopter/dp/B07PDPGFQY/ref=dp_prsubs_1?pd_rd_i=B07PDPGFQY&psc=1)
* [Radio Reciever: FrSky XM+](https://www.amazon.com/FrSky-Range-Receiver-Failsafe-Support/dp/B073PXL55X/ref=sr_1_21?crid=2Z66DXOEYGHKX&dchild=1&keywords=frsky+receiver&qid=1620955904&sprefix=frksy+%2Caps%2C164&sr=8-21)
* [Radio Transmitter: FrSky Q9 Lite](https://www.amazon.com/FrSky-Transmitter-Protocol-Airplane-Helicopter/dp/B07RQ5BCNG/ref=sr_1_8?crid=T5EQATLP789V&dchild=1&keywords=xm%2B%2Breceiver%2Bfrsky&qid=1620955835&sprefix=xm%2B%2Breceiver%2Caps%2C268&sr=8-8&th=1)
* [NUC: NUC7i7DNK1E](https://www.amazon.com/Intel-Business-Mini-Technology-BLKNUC7i7DNK1E/dp/B07BR7LK7C/ref=sr_1_1?dchild=1&keywords=nuc7i7dnk&qid=1614280581&sr=8-1)
* [Wireless USB Adapter](https://www.amazon.com/Panda-Wireless-PAU06-300Mbps-Adapter/dp/B00JDVRCI0/ref=sr_1_3?crid=2RW5KHLKJOP1F&dchild=1&keywords=panda+wireless+pau06&qid=1619537308&refinements=p_85%3A2470955011&rnid=2470954011&rps=1&sprefix=panda+wireless+pa%2Caps%2C152&sr=8-3)
* [Router](https://www.amazon.com/Panda-Wireless-PAU06-300Mbps-Adapter/dp/B00JDVRCI0/ref=sr_1_3?crid=2RW5KHLKJOP1F&dchild=1&keywords=panda+wireless+pau06&qid=1619537308&refinements=p_85%3A2470955011&rnid=2470954011&rps=1&sprefix=panda+wireless+pa%2Caps%2C152&sr=8-3)
* [SDR: USRP B210](https://www.ettus.com/all-products/ub210-kit/)
* [TPU 3D filament](https://www.amazon.com/PolyFlex-3-00-mm-750g-Yellow/dp/B00YXBO1UW/ref=sr_1_5?dchild=1&keywords=tpu+2.85mm&qid=1617384426&sr=8-5)
* [Nylon Bridge 3d filament](https://www.amazon.com/Printer-Filament-1-75mm-Dimensional-Accuracy/dp/B01MXDJ3IL/ref=sr_1_10?dchild=1&keywords=nylon+910+3mm&qid=1617385211&sr=8-10)
* [3D Printer](https://www.amazon.com/LulzBot-B07PFQQSR9-TAZ-Workhorse-Edition/dp/B07PFQQSR9/ref=sr_1_4?dchild=1&keywords=lulzbot&qid=1622753689&sr=8-4)

### Construction


### Flight Code

## Design Validation
### UAV Endurance Testing
For the endurance testing, [this script](https://github.com/buczek-j/BasicArducopter/blob/wines-powertest/power_test.py) was used to automate the process. The enduracne test outlined in the script is shown below:
![](https://github.com/buczek-j/wines-wireless-uav/blob/main/doc/UAV_endurance_test.png)
The UAV took off, performed a loop, and checked if its battery was below the 8S LiPo nominal voltage of 28.8V. If the voltage was below nominal, then the UAV would land, otherwise, it continued for another loop. This method of testing is more accurate to determine the flight time of a UAV as the UAV was contantly in motion. A flight test that would have the UAV hover in place would most likely dislpay an even longer flight time as the UAV would not need to adjust motor speeds for motion or altitude changes. 

### UAV GPS Interference
