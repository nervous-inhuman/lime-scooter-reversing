
Lime Scooter Reversing 
=======================

## Description

The purpose of this repository is to create a source/central point of truth for all things Lime. 

Please collaborate and share any information you may have, all push requests are highly encouraged, let's build a database thats informative, helpful and most of all semi-legal.

--------

### Scooters
| Photo                                         | Manufacturer  | Model           | Manual     | Notes     |  
|  --                                           | ---           | ---             | ---        | --        | 
|  ![noidea](https://i.imgur.com/ZlH30AJ.jpg)   | ?             | ?               | N/A        | Without display, flat rear fender/brake; No longer deployed(?); Gen 0 (?)
|  ![okai](https://i.imgur.com/NzvMlJd.png)     | Okai          | Custom(?)       | N/A        | "Lime recalled all the scooters made by Okai in its fleet worldwide."; Flat read fender/brake; Gen 1 (?)  
|  ![ES2](https://i.imgur.com/73wa8GJ.jpg)      | Segway        | Kickscooter ES2 | http://www.segway.com/media/2272/25612-00001_aa-kickscooter-user-manual-en.pdf            | Scooter has it's own BT; Gen 2 (?)
|  ![SJ25](https://i.imgur.com/7Mno79i.png) ![okai](https://i.imgur.com/n8F8iaf.jpg)![okai](https://i.imgur.com/PyMBqDM.jpg)![okai](https://i.imgur.com/nChRz0X.jpg)![okai](https://i.imgur.com/VdqvsBN.jpg)![okai](https://i.imgur.com/IYYR47g.jpg)![okai](https://i.imgur.com/GndnBEB.jpg)      | Lime          | LimeS SJ2.5			| N/A        | Gen 2.5; Manufactured by `Dong Guan Honglin Industrial Co. Ltd`
|  ![SJ3](https://i.imgur.com/ZOKGUAc.jpg) ![SJ3](https://i.imgur.com/8qz5Shr.jpg)     | Lime          | LimeS SJ3(?)    | N/A        | [Linux, Not deployed yet (?); Gen 3](https://www.li.me/blog/lime-s-gen-3-electric-scooter-transform-micro-mobility)

--------

### Segway ES2 scooter sections
Apparentely the scooter is divided in 3 main sections
1) the handle bar, contains the bluetooth and the speedometer, also the main on/off button, without it, you won't be able to start the scooter, ES2 models from bird, only need to replace this part in order to work as "zombie scooters".

2) the "main pole" this contains the battery, the control board, an extra battery and the "big green box", lime scooters are modified somehow and expose an external cable to control the main motor computer. so replacing the main control board will be a must

3) the base of the scooter, contains led drivers and motor mount, no locking is performed here.

Beware that because the scooters are protected they lock themselves into non working mode, a hard replacement of parts needs to be done.

### Trackers  
Spotted in the wild:

| Model         | Spotted on  |  
| ------------- | ----------- | 
| LBCAT-S-EU    | SJ2.5       |
| LBCATSL-EU_V02|             |
| LBCATSL-EU_V03| ES2         |


Seems to share same internals as the `LBCAT-(H|B)`, minus keypad daughterboard.

Shows up as BLE device, with naming format `lime-XXXXXXXX` and OUI `18:62:E4 - Texas Instruments`.
Might be `CC2540`?

![lbcat_uart](https://i.imgur.com/bKcM6Wa.png)
![lbcat](https://i.imgur.com/B6msfgl.png)
![lbcat_closeup](https://i.imgur.com/WkkuX6L.png)


```
LTE Modem: Qualcomm MDM9207(?)
DRAM: Nanya xxxx
BLE: TI CC2540(?)
```

##### Docs 
- [FCC ID](https://fccid.io/2APB2)
- [User Manual](https://fccid.io/2APB2LBCAT/Users-Manual/Users-Manual-3863957)
- [External Photos](https://fccid.io/2APB2LBCAT/External-Photos/External-Photos-3863955)
- [Internal Photos](https://fccid.io/2APB2LBCAT/Internal-Photos/Internal-Photos-3863956)
----------
#### Misc

- [Tech Stack](https://stackshare.io/lime/lime)
- [Mathew Garrett - Reversing Article](https://www.nzherald.co.nz/business/news/article.cfm?c_id=3&objectid=12163221) 
