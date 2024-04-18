Question 1: What is the ratio to total order from sales report?

SQL Queries: 
SELECT Round(ratio, 2) as ratio, total_order FROM sales_report
ORDER BY total_order DESC
Limit 10

Answer: 
This shows the ratio to total_order from sales_report.

Looking at this bar chart shows more quantities ordered did not have an effect on ratio of sales.

sample size of 10

Results

|ratio              |total_order|
|-------------------|-----------|
|0.22               |456        |
|0.24               |334        |
|0.06               |319        |
|0.06               |290        |
|0.06               |253        |
|0.71               |250        |
|0.46               |189        |
|0.59               |167        |
|0.02               |146        |
|0.02               |112        |






Question 2: What is the restocking lead time for each product?

SQL Queries: 
SELECT  name,  stock_level, restocking_lead_time FROM products

ORDER BY name,  restocking_lead_time DESC

Answer:
This shows the restocking lead time for each product.

The picture show the stock level for each product did not affect the restocking lead time

sample size of 10


|name                                               |stock_level|restocking_lead_time|
|---------------------------------------------------|-----------|--------------------|
|PC gaming speakers                                 |100        |1                   |
| Women's Colorblock Tee White                      |0          |8                   |
| Men's Quilted Insulated Vest Black                |32         |8                   |
| Women's Scoop Neck Tee Black                      |73         |6                   |
| Bongo Cupholder Bluetooth Speaker                 |115        |8                   |
|Aluminum Handy Emergency Flashlight                |90         |9                   |
| Men's Short Sleeve Hero Tee Charcoal              |104        |12                  |
| Women's Short Sleeve Tri-blend Badge Tee Grey     |33         |15                  |
| Sunglasses                                        |2086       |6                   |
|Red Shine 15 oz Mug                                |1417       |20                  |
|Recycled Paper Journal Set                         |740        |5                   |
| Women's Scoop Neck Tee Black                      |154        |5                   |
| Onesie Green                                      |9          |5                   |
| Learning Thermostat 3rd Gen-USA - White           |1142       |5                   |
|Android Stretch Fit Hat                            |8          |5                   |
| Men's Quilted Insulated Vest Battleship Grey      |39         |5                   |
| Dress Socks                                       |20         |6                   |
|Ballpoint Stylus Pen                               |0          |6                   |
| Women's Fleece Hoodie Black                       |0          |6                   |
|22 oz  Bottle Infuser                              |1944       |7                   |
| Women's Short Sleeve Hero Tee Sky Blue            |2          |7                   |
| Infant Short Sleeve Tee Green                     |52         |7                   |
| Learning Thermostat 3rd Gen-USA - Stainless Steel |2525       |7                   |
|Android 17oz Stainless Steel Sport Bottle          |283        |8                   |
| Men's Short Sleeve Hero Tee Charcoal              |61         |8                   |
| Women's Convertible Vest-Jacket Black             |44         |8                   |
| Device Holder Sticky Pad                          |0          |8                   |
| Womens 3/4 Sleeve Baseball Raglan Heather/Black   |31         |9                   |
| Baby Essentials Set                               |77         |10                  |
| Mood Original Window Decal                        |0          |11                  |
| Youth Short Sleeve Tee Red                        |10         |11                  |
| Luggage Tag                                       |0          |11                  |
| Men's 100% Cotton Short Sleeve Hero Tee White     |0          |11                  |
| Men's Short Sleeve Performance Badge Tee Black    |7          |11                  |
| Men's Long & Lean Tee Charcoal                    |13         |12                  |
|Android Toddler Short Sleeve T-shirt Pink          |28         |12                  |
| Women's V-Neck Tee Charcoal                       |8          |12                  |
| Men's Vintage Badge Tee Black                     |578        |13                  |
| Women's 1/4 Zip Performance Pullover Two-Tone Blue|28         |13                  |
| Men's Pullover Hoodie Grey                        |27         |13                  |
|Colored Pencil Set                                 |367        |13                  |
| Men's Short Sleeve Badge Tee Charcoal             |0          |13                  |
| Toddler Sports T-shirt Red                        |9          |13                  |
| Infant Zip Hood Pink                              |54         |13                  |
| Women's Vintage Hero Tee Black                    |153        |14                  |
| Women's Convertible Vest-Jacket Sea Foam Green    |5          |14                  |
| Women's Performance Full Zip Jacket Black         |0          |14                  |
| Men's Quilted Insulated Vest Battleship Grey      |5          |14                  |
| Men's Colorblock Tee White/Heather                |0          |14                  |
|Android Stretch Fit Hat                            |10         |14                  |
| Men's Short Sleeve Hero Tee Heather               |23         |14                  |
| Youth Sports Tee Navy                             |29         |14                  |
| Toddler Short Sleeve Tee Red                      |7          |14                  |
|Android Men's Take Charge Short Sleeve Tee Purple  |21         |14                  |
| Men's Long & Lean Tee Grey                        |100        |15                  |
| Women's V-Neck Tee Charcoal                       |6          |15                  |
| Women's Recycled Fabric Tee                       |1          |15                  |
| Women's Short Sleeve Hero Tee Sky Blue            |0          |16                  |
| Onesie Red                                        |31         |16                  |
| Women's Yoga Jacket Black                         |0          |16                  |
| Men's Airflow 1/4 Zip Pullover Lapis              |31         |17                  |
| Youth Short Sleeve T-shirt Royal Blue             |5          |17                  |
| Women's Short Sleeve Performance Tee Charcoal     |14         |17                  |
| Men's Short Sleeve Tee                            |0          |17                  |
| Toddler Short Sleeve Tee Red                      |4          |17                  |
| Men's Short Sleeve Hero Tee Charcoal              |182        |19                  |
|Android Onesie Gold                                |2          |19                  |
|Crunch Noise Dog Toy                               |352        |9                   |
| Men's Vintage Badge Tee White                     |210        |9                   |
|20 oz Stainless Steel Insulated Tumbler            |652        |2                   |
| Mobile Phone Vent Mount                           |0          |7                   |
| Learning Thermostat 3rd Gen-USA - Stainless Steel |0          |8                   |
|Android Men's Paradise Short Sleeve Tee Olive      |11         |8                   |
| Women's Short Sleeve Tri-blend Badge Tee Grey     |1          |11                  |
| Toddler Raglan Shirt Blue Heather/Navy            |0          |11                  |
| Men's Quilted Insulated Vest Black                |17         |14                  |
| Men's 100% Cotton Short Sleeve Hero Tee White     |41         |15                  |
| Power Bank                                        |210        |7                   |
| 4400mAh Power Bank                                |65         |7                   |
|Yoga Mat Purple                                    |13         |17                  |
|Yoga Mat Blue                                      |60         |15                  |
| G Noise-reducing Bluetooth Headphones             |132        |7                   |
| Sunglasses                                        |376        |8                   |
|USB wired soundbar - in store only                 |15         |2                   |
|Recycled Mouse Pad                                 |1756       |39                  |
|Android Men's Short Sleeve Hero Tee Heather        |19         |17                  |
| Toddler Sports T-shirt Red                        |0          |5                   |
| Men's Long & Lean Tee Charcoal                    |20         |5                   |
|Plastic Sliding Flashlight                         |0          |5                   |
| Men's Short Sleeve Performance Badge Tee Black    |8          |5                   |
|Android Women's Short Sleeve Badge Tee Dark Heather|5          |6                   |
| Tote Bag                                          |155        |6                   |
| Men's Short Sleeve Badge Tee Charcoal             |105        |6                   |
| Women's Short Sleeve Hero Tee Grey                |117        |6                   |
| Men's Performance 1/4 Zip Pullover Heather/Black  |0          |6                   |
| Toddler Short Sleeve T-shirt Grey                 |93         |6                   |
| Men's Vintage Badge Tee Sage                      |390        |6                   |
|Android Onesie Gold                                |53         |6                   |
|Android Infant Short Sleeve Tee Pink               |21         |7                   |
| Toddler Sports T-shirt Red                        |13         |7                   |
| Zipper-front Sports Bag                           |0          |7                   |
|Android Women's Long Sleeve Blended Cardigan Grey  |29         |7                   |
| Vintage Henley Grey/Black                         |1          |7                   |
| Women's Short Sleeve Hero Tee White               |65         |7                   |
| Women's Yoga Jacket Black                         |34         |8                   |
| Pet Feeding Mat                                   |0          |8                   |
| Women's Vintage Hero Tee Black                    |213        |9                   |
| Men's Quilted Insulated Vest Black                |51         |9                   |
| Women's Short Sleeve Performance Tee Pewter       |1          |10                  |
| Cam Outdoor Security Camera - USA                 |4683       |10                  |
| Men's Short Sleeve Performance Badge Tee Pewter   |131        |10                  |
|Gift Card- $100.00                                 |77         |10                  |
| Tube Power Bank                                   |0          |11                  |
| Men's Bike Short Sleeve Tee Charcoal              |70         |11                  |
|Android Stretch Fit Hat S/M                        |53         |12                  |
| Women's Softshell Jacket Black/Grey               |0          |13                  |
| Men's Short Sleeve Hero Tee  White                |3          |13                  |
| Women's Short Sleeve Tee                          |0          |13                  |
| Youth Sports Tee Navy                             |42         |14                  |
| Men's Lightweight Microfleece Jacket Black        |8          |14                  |
| Women's 1/4 Zip Performance Pullover Black        |35         |14                  |
|Android Toddler Short Sleeve T-shirt Aqua          |25         |15                  |
| Toddler Hoodie Royal Blue                         |45         |15                  |
| Women's Yoga Pants                                |0          |15                  |
| Youth Girl Hoodie                                 |5          |15                  |
| Women's Performance Hero Tee Gunmetal             |25         |15                  |
|Android Stretch Fit Hat                            |41         |16                  |
| Leather Journal-Brown                             |0          |16                  |
| Women's Shell Jacket Blue/Black                   |0          |16                  |
| Men's Long & Lean Tee Grey                        |21         |16                  |
|Android Infant Short Sleeve Tee Pink               |32         |17                  |
|Android BTTF Cosmos Graphic Tee                    |5          |17                  |
| Men's Performance Full Zip Jacket Black           |70         |18                  |
|Android BTTF Moonshot Graphic Tee                  |16         |18                  |
| Onesie Green                                      |49         |19                  |
| Men's Colorblock Tee White/Heather                |10         |19                  |
|25L Classic Rucksack                               |114        |6                   |
|Android Women's Short Sleeve Badge Tee Dark Heather|0          |7                   |
| Men's Short Sleeve Hero Tee Heather               |1          |7                   |
| Learning Thermostat 3rd Gen-USA - Copper          |564        |9                   |
| Men's  Zip Hoodie                                 |156        |14                  |
|Android Men's Pep Rally Short Sleeve Tee Navy      |26         |18                  |
| 17oz Stainless Steel Sport Bottle                 |0          |18                  |
|Android Men's Short Sleeve Hero Tee White          |38         |11                  |
|Android Men's Short Sleeve Tri-blend Hero Tee Grey |3          |16                  |
|Electronics Accessory Pouch                        |568        |29                  |
| Men's Pullover Hoodie Grey                        |33         |5                   |
| Men's Vintage Badge Tee Black                     |677        |8                   |
| Men's Short Sleeve Badge Tee Charcoal             |12         |11                  |
| Women's Short Sleeve Hero Dark Grey               |50         |5                   |
| Women's Short Sleeve Badge Tee Navy               |8          |17                  |
| Men's Airflow 1/4 Zip Pullover Black              |8          |9                   |
|Android RFID Journal                               |86         |9                   |
| Women's Yoga Jacket Black                         |33         |6                   |
|Android Men's Long & Lean Badge Tee Charcoal       |65         |18                  |
|Satin Black Ballpoint Pen                          |477        |2                   |
| Snapback Hat Black                                |105        |3                   |
|Rubber Grip Ballpoint Pen 4 Pack                   |1791       |3                   |
|Android Men's Pep Rally Short Sleeve Tee Navy      |7          |5                   |
| Women's Scoop Neck Tee Black                      |23         |5                   |
| Onesie Red/Graphite                               |14         |6                   |
|Yoga Mat Blue                                      |0          |6                   |
|Women's Performance Full Zip Jacket Black          |9          |6                   |
| Men's Short Sleeve Tee                            |5          |7                   |
| Women's V-Neck Tee Charcoal                       |4          |7                   |
| Toddler 1/4 Zip Fleece Pewter                     |33         |7                   |
| Toddler Short Sleeve Tee Red                      |12         |7                   |
| Women's Short Sleeve Badge Tee Grey               |13         |8                   |
| 17 oz Double Wall Stainless Steel Insulated Bottle|0          |8                   |
| Men's Pullover Hoodie Grey                        |14         |8                   |
| Women's Short Sleeve Performance Tee Pewter       |6          |8                   |
|Men's Weatherblock Shell Jacket Black              |4          |9                   |
| Women's Lightweight Microfleece Jacket            |5          |9                   |
|Android BTTF Cosmos Graphic Tee                    |6          |10                  |
| Spiral Journal with Pen                           |4668       |10                  |
|Android Youth Short Sleeve T-shirt Aqua            |4          |10                  |
| Tri-blend Hoodie Grey                             |11         |10                  |
|Android Men's Outerstellar Short Sleeve Tee Black  |13         |10                  |
| Women's Convertible Vest-Jacket Sea Foam Green    |32         |11                  |
| Youth Short Sleeve T-shirt Green                  |12         |11                  |
| Youth Girl Tee Green                              |0          |11                  |
| Protect Smoke + CO White Battery Alarm-USA        |325        |11                  |
| Women's Scoop Neck Tee White                      |50         |11                  |
| Men's Short Sleeve Performance Badge Tee Pewter   |15         |11                  |
| Women's Short Sleeve Tri-blend Badge Tee Charcoal |3          |11                  |
| Women's Short Sleeve Performance Tee Pewter       |8          |12                  |
|Women's Weatherblock Shell Jacket Black            |8          |12                  |
| Snapback Hat Black                                |0          |12                  |
|Android Youth Short Sleeve T-shirt Aqua            |77         |13                  |
|Women's  Short Sleeve Hero Tee Black               |37         |13                  |
|Android Men's Take Charge Short Sleeve Tee Purple  |16         |13                  |
|Yoga Block                                         |0          |13                  |
| Women's Long Sleeve Tee Lavender                  |18         |13                  |
|Android Men's Long & Lean Badge Tee Charcoal       |27         |13                  |
| Infant Zip Hood Pink                              |0          |14                  |
| Toddler Raglan Shirt Blue Heather/Navy            |20         |14                  |
| Custom Decals                                     |4536       |14                  |
|Android Infant Short Sleeve Tee Pewter             |2          |14                  |
| Men's Short Sleeve Hero Tee Black                 |40         |14                  |
| Women's Fleece Hoodie Black                       |1          |14                  |
|Android Men's Take Charge Short Sleeve Tee Purple  |7          |15                  |
| Women's Short Sleeve Hero Dark Grey               |2          |15                  |
|Android BTTF Moonshot Graphic Tee                  |13         |15                  |
| Tri-blend Hoodie Grey                             |3          |15                  |
| Men's 100% Cotton Short Sleeve Hero Tee Navy      |74         |15                  |
| Women's Short Sleeve Tri-blend Badge Tee Charcoal |111        |16                  |
| Men's Vintage Badge Tee Sage                      |3          |16                  |
| Men's Short Sleeve Hero Tee Charcoal              |23         |18                  |
| Women's Short Sleeve Hero Tee Charcoal            |4          |19                  |
| Tri-blend Hoodie Grey                             |0          |19                  |
| Men's Short Sleeve Hero Tee Black                 |20         |19                  |
| Men's Long & Lean Tee Grey                        |5          |6                   |
| Men's Short Sleeve Hero Tee Black                 |275        |6                   |
|Android Women's Fleece Hoodie                      |21         |13                  |
|Android Men's Vintage Henley                       |37         |15                  |
|Four Color Retractable Pen                         |2450       |22                  |
| Cam Indoor Security Camera - USA                  |2615       |42                  |
|Ballpoint Stylus Pen                               |942        |5                   |
| Car Clip Phone Holder                             |205        |5                   |
| Women's Vintage Hero Tee White                    |94         |6                   |
|Android Onesie Gold                                |8          |6                   |
| Men's Lightweight Microfleece Jacket Black        |11         |7                   |
| Men's Performance 1/4 Zip Pullover Heather/Black  |2          |10                  |
| Toddler Raglan Shirt Blue Heather/Navy            |12         |10                  |
| Women's Short Sleeve Hero Tee Sky Blue            |8          |11                  |
| Women's Short Sleeve Hero Tee Black               |200        |11                  |
| Men's 3/4 Sleeve Henley                           |0          |11                  |
| Canvas Tote Natural/Navy                          |0          |12                  |
|Android Toddler Short Sleeve T-shirt Aqua          |99         |12                  |
| Toddler Short Sleeve T-shirt Royal Blue           |2          |12                  |
| Tri-blend Hoodie Grey                             |34         |12                  |
|Switch Tone Color Crayon Pen                       |388        |12                  |
| Men's Short Sleeve Hero Tee Charcoal              |59         |12                  |
|Android Men's Outerstellar Short Sleeve Tee Black  |12         |12                  |
| Men's Performance 1/4 Zip Pullover Heather/Black  |19         |12                  |
| Men's Colorblock Tee White/Heather                |2          |13                  |
| Toddler Short Sleeve T-shirt Royal Blue           |12         |14                  |
| Women's Lightweight Microfleece Jacket            |13         |14                  |
| Men's Watershed Full Zip Hoodie Grey              |0          |14                  |
| Women's Lightweight Microfleece Jacket            |3          |15                  |
| Men's Long & Lean Tee Charcoal                    |0          |16                  |
| Toddler Sports T-shirt Red                        |6          |16                  |
| Men's Bike Short Sleeve Tee Charcoal              |29         |16                  |
| Hard Cover Journal                                |0          |17                  |
| Women's Convertible Vest-Jacket Black             |37         |17                  |
| Men's Watershed Full Zip Hoodie Grey              |7          |17                  |
|Android Women's Short Sleeve Badge Tee Dark Heather|7          |18                  |
| Women's Fleece Hoodie                             |1          |19                  |
| Men's Performance Full Zip Jacket Black           |54         |12                  |
|Suitcase Organizer Cubes                           |342        |7                   |
|7 Dog Frisbee                                      |154        |11                  |
|Android Men's Outerstellar Short Sleeve Tee Black  |3          |6                   |
| Men's Microfiber 1/4 Zip Pullover Blue/Indigo     |9          |7                   |
| Twill Cap                                         |1997       |2                   |
| Men's Typography Short Sleeve Tee                 |1          |6                   |
| Blackout Cap                                      |415        |6                   |
|Android Toddler Short Sleeve T-shirt Aqua          |16         |6                   |
| Women's Short Sleeve Hero Tee White               |19         |6                   |
| Youth Short Sleeve Tee White                      |5          |6                   |
| Men's Vintage Henley                              |26         |7                   |
| Men's Short Sleeve Hero Tee Heather               |13         |7                   |
| Toddler Short Sleeve T-shirt Royal Blue           |22         |7                   |
| Men's Short Sleeve Hero Tee Charcoal              |25         |8                   |
| Men's Quilted Insulated Vest Black                |27         |8                   |
|Android Infant Short Sleeve Tee Pink               |18         |8                   |
| Onesie Red                                        |37         |8                   |
| Men's 100% Cotton Short Sleeve Hero Tee Black     |50         |8                   |
| Women's Long Sleeve Tee Lavender                  |9          |8                   |
| Women's Short Sleeve Hero Tee Red Heather         |40         |9                   |
| Men's Short Sleeve Performance Badge Tee Charcoal |5          |9                   |
|Gunmetal Roller Ball Pen                           |0          |9                   |
| Men's Watershed Full Zip Hoodie Grey              |57         |9                   |
| Women's Performance Golf Polo Blue                |6          |10                  |
| Women's Convertible Vest-Jacket Black             |0          |11                  |
| Men's Vintage Henley                              |65         |11                  |
| Men's Vintage Badge Tee White                     |16         |11                  |
|Android Youth Short Sleeve T-shirt Pewter          |38         |12                  |
| Women's Scoop Neck Tee Black                      |91         |12                  |
| Men's Short Sleeve Hero Tee Light Blue            |2          |12                  |
| Womens 3/4 Sleeve Baseball Raglan Heather/Black   |32         |13                  |
| Toddler Short Sleeve T-shirt Royal Blue           |0          |13                  |
| Men's Short Sleeve Performance Badge Tee Charcoal |9          |13                  |
| Youth Baseball Raglan Heather/Black               |2          |13                  |
| 17 oz Double Wall Stainless Steel Insulated Bottle|633        |14                  |
| Men's Performance Full Zip Jacket Black           |0          |14                  |
|Android Toddler Short Sleeve T-shirt Pewter        |6          |14                  |
|Android Men's Pep Rally Short Sleeve Tee Navy      |19         |14                  |
| Baby on Board Window Decal                        |0          |15                  |
| Women's Short Sleeve Badge Tee Grey               |26         |15                  |
| Wool Heather Cap Heather/Black                    |0          |15                  |
| Women's Vintage Hero Tee White                    |125        |16                  |
| Women's Tee Grey                                  |12         |16                  |
| Men's Vintage Henley                              |53         |17                  |
| Women's Fleece Hoodie                             |0          |17                  |
|Android Onesie Gold                                |2          |18                  |
| Men's Long Sleeve Raglan Ocean Blue               |36         |18                  |
|Android Men's Short Sleeve Hero Tee Heather        |68         |19                  |
| Women's 1/4 Zip Jacket Charcoal                   |12         |19                  |
| Women's Short Sleeve Hero Tee Black               |173        |19                  |
| Kick Ball                                         |723        |5                   |
| Women's Short Sleeve Hero Tee White               |41         |5                   |
|UpCycled Handlebar Bag                             |107        |12                  |
| Women's Short Sleeve Tri-blend Badge Tee Charcoal |43         |18                  |
| Men's Lightweight Microfleece Jacket Black        |20         |19                  |
| Men's 100% Cotton Short Sleeve Hero Tee Navy      |7          |5                   |
| Men's Short Sleeve Performance Badge Tee Black    |2          |6                   |
| Women's 1/4 Zip Jacket Charcoal                   |0          |6                   |
| Youth Short Sleeve T-shirt Yellow                 |38         |7                   |
| Men's Microfiber 1/4 Zip Pullover Blue/Indigo     |0          |7                   |
| Women's Scoop Neck Tee White                      |10         |7                   |
|Metal Texture Roller Pen                           |0          |8                   |
| Women's Short Sleeve Hero Dark Grey               |7          |9                   |
| Men's  Zip Hoodie                                 |0          |10                  |
| Women's Long Sleeve Tee Lavender                  |1          |10                  |
| Toddler Short Sleeve Tee Red                      |2          |10                  |
| Women's Yoga Pants                                |4          |10                  |
| Men's Long & Lean Tee Charcoal                    |42         |11                  |
| Women's Short Sleeve Tee                          |4          |12                  |
| Women's Yoga Jacket Black                         |8          |12                  |
| Toddler Short Sleeve Tee Red                      |17         |13                  |
| Women's Short Sleeve Hero Dark Grey               |5          |13                  |
| Infant Short Sleeve Tee White                     |31         |14                  |
| Men's Vintage Tank                                |74         |15                  |
| Women's Short Sleeve Hero Dark Grey               |2          |17                  |
| Women's 3/4 Sleeve Baseball Raglan Heather/Black  |0          |17                  |
| Toddler 1/4 Zip Fleece Pewter                     |44         |17                  |
| Trucker Hat                                       |0          |17                  |
| Men's Pullover Hoodie Grey                        |17         |18                  |
| Men's Short Sleeve Hero Tee Charcoal              |1          |19                  |
|BLM Sweatshirt                                     |0          |19                  |
| Men's Vintage Badge Tee Sage                      |277        |19                  |
| Onesie Red                                        |20         |19                  |
| Men's 100% Cotton Short Sleeve Hero Tee Black     |193        |19                  |
|Yoga Mat                                           |54         |5                   |
|Pen Pencil & Highlighter Set                       |1939       |5                   |
| Youth Short Sleeve Tee Red                        |40         |6                   |
| Men's Lightweight Microfleece Jacket Black        |9          |6                   |
|Android Men's Vintage Tank                         |9          |6                   |
| Men's Short Sleeve Hero Tee Black                 |27         |6                   |
| Men's Performance Full Zip Jacket Black           |27         |6                   |
|Android Men's Short Sleeve Hero Tee Heather        |126        |8                   |
|Keyboard DOT Sticker                               |189        |9                   |
|Android Onesie Gold                                |34         |9                   |
|Foam Can and Bottle Cooler                         |4495       |10                  |
| Men's Bike Short Sleeve Tee Charcoal              |34         |11                  |
| Men's Convertible Vest-Jacket Pewter              |1          |11                  |
| Vintage Henley Grey/Black                         |23         |11                  |
|8 pc Android Sticker Sheet                         |613        |12                  |
| Men's Bayside Graphic Tee                         |9          |14                  |
| Youth Girl Hoodie                                 |7          |15                  |
|Android Youth Short Sleeve T-shirt Aqua            |0          |16                  |
| Women's Short Sleeve Hero Tee Red Heather         |25         |17                  |
| Men's Fleece Hoodie Black                         |0          |18                  |
| Men's Vintage Badge Tee White                     |74         |18                  |
| Learning Thermostat 3rd Gen-USA - Copper          |0          |19                  |
| Women's Vintage Hero Tee Lavender                 |9          |19                  |
| Women's Vintage Hero Tee Platinum                 |65         |19                  |
|Waterproof Gear Bag                                |261        |15                  |
|Android Wool Heather Cap Heather/Black             |305        |9                   |
|UpCycled Bike Saddle Bag                           |79         |12                  |
| Collapsible Pet Bowl                              |50         |6                   |
| Women's Recycled Fabric Tee                       |16         |10                  |
| Vintage Henley Grey/Black                         |95         |10                  |
| Men's Short Sleeve Hero Tee Light Blue            |3          |10                  |
| Men's Short Sleeve Tee                            |1          |14                  |
|Android Women's Long Sleeve Blended Cardigan Grey  |28         |18                  |
|Android Women's Short Sleeve Badge Tee Dark Heather|19         |15                  |
| Pet Feeding Mat                                   |83         |18                  |
| Women's Short Sleeve Hero Dark Grey               |5          |5                   |
| 5-Panel Cap                                       |87         |5                   |
|Android Wool Heather Cap Heather/Black             |0          |5                   |
| Men's Vintage Badge Tee Black                     |135        |5                   |
|Android Men's Engineer Short Sleeve Tee Charcoal   |22         |6                   |
|Android Men's Long & Lean Badge Tee Charcoal       |0          |7                   |
| Men's Pullover Hoodie Grey                        |24         |8                   |
| Women's Lightweight Microfleece Jacket            |0          |8                   |
| Slim Utility Travel Bag                           |0          |8                   |
| Women's Short Sleeve Badge Tee Navy               |25         |9                   |
| Protect Smoke + CO White Battery Alarm - CA       |25         |9                   |
| Women's Vintage Hero Tee Lavender                 |26         |10                  |
| Women's Yoga Jacket Black                         |0          |10                  |
| Women's Short Sleeve Performance Tee Charcoal     |11         |10                  |
| Women's Long Sleeve Blended Cardigan Charcoal     |42         |10                  |
| Men's Vintage Badge Tee White                     |156        |11                  |
|Android Men's  Zip Hoodie                          |7          |11                  |
|Spiral Notebook and Pen Set                        |6708       |11                  |
| Youth Girl Tee Green                              |5          |11                  |
| G Noise-reducing Bluetooth Headphones             |0          |11                  |
| Women's Vintage Hero Tee Lavender                 |31         |11                  |
| Women's Short Sleeve Hero Tee Heather             |9          |12                  |
| Slim Utility Travel Bag                           |516        |12                  |
| Men's Long Sleeve Raglan Ocean Blue               |0          |13                  |
| Men's Vintage Badge Tee Sage                      |74         |14                  |
| Men's Vintage Tank                                |7          |14                  |
| Youth Short Sleeve Tee Red                        |0          |14                  |
| Women's Performance Golf Polo Blue                |0          |14                  |
|Android Men's Outerstellar Short Sleeve Tee Black  |24         |15                  |
| Men's Long & Lean Tee Charcoal                    |309        |16                  |
| Women's Yoga Jacket Black                         |5          |16                  |
| Men's Watershed Full Zip Hoodie Grey              |105        |17                  |
| Men's Long & Lean Tee Charcoal                    |22         |17                  |
| Women's Short Sleeve Hero Tee Sky Blue            |0          |17                  |
| Men's Airflow 1/4 Zip Pullover Lapis              |1          |17                  |
| Men's Convertible Vest-Jacket Pewter              |0          |17                  |
|Android Men's Long Sleeve Badge Crew Tee Heather   |9          |19                  |
| Youth Short Sleeve T-shirt Yellow                 |46         |19                  |
| Men's Short Sleeve Performance Badge Tee Pewter   |29         |15                  |
| 5-Panel Snapback Cap                              |219        |8                   |
| Women's Short Sleeve Hero Tee Heather             |1          |7                   |
| Men's Short Sleeve Hero Tee White                 |86         |10                  |
|Women's  Short Sleeve Hero Tee Black               |23         |11                  |
| Women's Vintage Hero Tee Black                    |332        |19                  |
| Women's Short Sleeve Hero Tee Grey                |52         |19                  |
| Tube Power Bank                                   |72         |8                   |
| Laptop and Cell Phone Stickers                    |1516       |3                   |
|Android Men's Paradise Short Sleeve Tee Olive      |11         |5                   |
|Android Men's Long & Lean Badge Tee Charcoal       |30         |5                   |
|Gift Card - $50.00                                 |0          |5                   |
| Youth Short Sleeve Tee Red                        |13         |5                   |
| Infant Short Sleeve Tee Royal Blue                |2          |5                   |
| Women's Vintage Hero Tee White                    |19         |6                   |
| Youth Short Sleeve Tee White                      |14         |6                   |
|Seat Pack Organizer                                |0          |7                   |
| Men's Short Sleeve Badge Tee Charcoal             |46         |7                   |
|Men's Weatherblock Shell Jacket Black              |2          |7                   |
|Android Luggage Tag                                |0          |7                   |
|Android Men's Outerstellar Short Sleeve Tee Black  |2          |8                   |
| Baby Essentials Set                               |346        |8                   |
| Leather Journal                                   |181        |8                   |
| 22 oz Water Bottle                                |1482       |9                   |
| Men's Airflow 1/4 Zip Pullover Lapis              |4          |9                   |
|Maze Pen                                           |324        |9                   |
| Men's 100% Cotton Short Sleeve Hero Tee White     |335        |9                   |
| Women's Vintage Hero Tee White                    |17         |9                   |
| Women's 1/4 Zip Jacket Charcoal                   |4          |10                  |
| Men's Vintage Tank                                |7          |10                  |
| Infant Zip Hood Royal Blue                        |30         |10                  |
| Cam Indoor Security Camera - USA                  |0          |10                  |
| Bongo Cupholder Bluetooth Speaker                 |0          |10                  |
|Android Men's Long & Lean Badge Tee Charcoal       |42         |11                  |
| Women's Fleece Hoodie Black                       |13         |11                  |
| Men's Performance Full Zip Jacket Black           |10         |11                  |
| Women's Quilted Insulated Vest Black              |2          |11                  |
| Collapsible Pet Bowl                              |0          |11                  |
|Ballpoint LED Light Pen                            |2098       |11                  |
| Men's Short Sleeve Hero Tee Charcoal              |41         |12                  |
|Android Men's Vintage Henley                       |0          |12                  |
|Gift Card - $250.00                                |0          |12                  |
| Toddler Hoodie Royal Blue                         |27         |12                  |
| Toddler Raglan Shirt Blue Heather/Navy            |9          |12                  |
| Women's Typography Short Sleeve Tee               |0          |13                  |
|Android Toddler Short Sleeve T-shirt Aqua          |26         |13                  |
| Youth Short Sleeve Tee Red                        |26         |13                  |
| Women's Performance Golf Polo Blue                |4          |13                  |
| Women's Long Sleeve Tee Lavender                  |29         |14                  |
|Android Men's Long Sleeve Badge Crew Tee Heather   |43         |14                  |
|25L Classic Rucksack                               |40         |15                  |
|Android Luggage Tag                                |32         |15                  |
| Toddler Short Sleeve T-shirt Royal Blue           |20         |15                  |
|Satin Black Ballpoint Pen                          |0          |16                  |
|Android Infant Short Sleeve Tee Pewter             |23         |16                  |
| Toddler 1/4 Zip Fleece Pewter                     |3          |16                  |
| Women's Short Sleeve Hero Tee Red Heather         |7          |16                  |
| Women's Short Sleeve Tri-blend Badge Tee Grey     |1          |16                  |
| Youth Short Sleeve Tee Red                        |15         |17                  |
| French Terry Cap                                  |0          |17                  |
| Women's Short Sleeve Hero Tee Sky Blue            |16         |18                  |
|Android Women's Long Sleeve Blended Cardigan Grey  |8          |18                  |
| Car Clip Phone Holder                             |0          |18                  |
| Youth Short Sleeve Tee Red                        |38         |18                  |
| Women's Tee Grey                                  |23         |19                  |
| Men's Short Sleeve Performance Badge Tee Charcoal |0          |19                  |
| Youth Girl Hoodie                                 |5          |19                  |
| Pet Feeding Mat                                   |69         |7                   |
| Men's Airflow 1/4 Zip Pullover Lapis              |23         |8                   |
| Women's Short Sleeve Hero Tee Sky Blue            |44         |9                   |
| Women's 3/4 Sleeve Baseball Raglan Heather/Black  |26         |9                   |
| Men's Short Sleeve Performance Badge Tee Charcoal |57         |14                  |
| Tri-blend Hoodie Grey                             |101        |15                  |
|Android BTTF Moonshot Graphic Tee                  |0          |15                  |
| Women's Short Sleeve Hero Tee Charcoal            |54         |16                  |
| Men's Short Sleeve Hero Tee Charcoal              |20         |19                  |
| Women's Lightweight Microfleece Jacket            |3          |19                  |
| Women's Performance Golf Polo Blue                |0          |19                  |
| Men's Vintage Henley                              |133        |9                   |
|Clip-on Compact Charger                            |1468       |11                  |
| Men's Short Sleeve Performance Badge Tee Navy     |21         |9                   |
|Rocket Flashlight                                  |242        |11                  |
| Stylus Pen w/ LED Light                           |2164       |39                  |
|Metal Texture Roller Pen                           |775        |3                   |
| Men's Watershed Full Zip Hoodie Grey              |25         |5                   |
| Mood Ninja Window Decal                           |94         |6                   |
| Women's Fleece Hoodie                             |11         |6                   |
| Onesie Heather                                    |37         |7                   |
| Men's Watershed Full Zip Hoodie Grey              |0          |7                   |
| Toddler Short Sleeve Tee Red                      |27         |8                   |
| Women's Tee Grey                                  |13         |8                   |
| Men's Bayside Graphic Tee                         |33         |8                   |
| Infant Zip Hood Pink                              |35         |8                   |
| Women's Vintage Hero Tee Platinum                 |13         |9                   |
|Women's Performance Full Zip Jacket Black          |11         |10                  |
| Men's Short Sleeve Hero Tee Heather               |29         |11                  |
| Infant Short Sleeve Tee Royal Blue                |33         |11                  |
|Android Women's Fleece Hoodie                      |0          |12                  |
| Pocket Bluetooth Speaker                          |0          |12                  |
| Men's Vintage Tee                                 |0          |12                  |
| Men's Quilted Insulated Vest Battleship Grey      |27         |12                  |
| Women's Long Sleeve Blended Cardigan Charcoal     |25         |13                  |
| Men's Short Sleeve Hero Tee Light Blue            |5          |13                  |
|Recycled Paper Journal Set                         |4975       |13                  |
|Women's Performance Full Zip Jacket Black          |33         |14                  |
| Youth Sports Tee Navy                             |37         |14                  |
| Women's Vintage Hero Tee Platinum                 |94         |15                  |
|Android Onesie Gold                                |29         |15                  |
| Men's 100% Cotton Short Sleeve Hero Tee White     |186        |16                  |
| Tri-blend Hoodie Grey                             |62         |16                  |
| Men's Short Sleeve Performance Badge Tee Black    |3          |17                  |
| Tri-blend Hoodie Grey                             |45         |17                  |
| Youth Baseball Raglan Heather/Black               |21         |18                  |
| Executive Umbrella                                |0          |18                  |
| Men's Vintage Badge Tee White                     |237        |18                  |
| Men's Short Sleeve Hero Tee Charcoal              |33         |18                  |
|Crunch Noise Dog Toy                               |0          |19                  |
| Women's Short Sleeve Tee                          |0          |14                  |
|Android BTTF Cosmos Graphic Tee                    |4          |15                  |
|Android Lifted Men's Short Sleeve Tee Blue         |14         |17                  |
| Men's Long Sleeve Raglan Ocean Blue               |10         |17                  |
| Men's Convertible Vest-Jacket Pewter              |0          |17                  |
| Women's V-Neck Tee Charcoal                       |77         |8                   |
| Women's Vintage Hero Tee Lavender                 |65         |17                  |
| Men's Weatherblock Shell Jacket Black             |5          |17                  |
| RFID Journal                                      |433        |3                   |
| Metallic Notebook Set                             |610        |5                   |
| Men's Short Sleeve Performance Badge Tee Charcoal |30         |5                   |
|Basecamp Explorer Powerbank Flashlight             |0          |5                   |
| Rucksack                                          |228        |5                   |
| Men's Short Sleeve Hero Tee White                 |39         |7                   |
|UpCycled Handlebar Bag                             |0          |7                   |
| Women's Lightweight Microfleece Jacket            |3          |7                   |
| Mood Original Window Decal                        |66         |8                   |
| Youth Short Sleeve Tee Red                        |1          |9                   |
|Men's Weatherblock Shell Jacket Black              |12         |10                  |
| Women's Performance Hero Tee Gunmetal             |1          |10                  |
| Men's Vintage Badge Tee White                     |120        |10                  |
| Men's Short Sleeve Hero Tee Black                 |39         |10                  |
|Waterproof Backpack                                |230        |10                  |
| Women's 1/4 Zip Jacket Charcoal                   |18         |10                  |
| Onesie Heather                                    |26         |11                  |
|Android Women's Short Sleeve Hero Tee Black        |1          |11                  |
|Gift Card - $25.00                                 |0          |11                  |
| Men's Short Sleeve Tee                            |2          |11                  |
| Women's Short Sleeve Badge Tee Navy               |15         |12                  |
| Infant Short Sleeve Tee Red                       |1          |13                  |
| Women's Quilted Insulated Vest White              |2          |13                  |
| Men's 100% Cotton Short Sleeve Hero Tee Navy      |66         |14                  |
| Men's 100% Cotton Short Sleeve Hero Tee Red       |146        |14                  |
| Women's Scoop Neck Tee White                      |27         |14                  |
| Onesie Green                                      |29         |15                  |
|Android Stretch Fit Hat                            |0          |15                  |
| Screen Cleaning Cloth                             |0          |15                  |
|Android Men's Pep Rally Short Sleeve Tee Navy      |1          |16                  |
|Android Men's Short Sleeve Hero Tee Heather        |84         |16                  |
| Men's Bike Short Sleeve Tee Charcoal              |53         |16                  |
| Women's Performance Hero Tee Gunmetal             |0          |17                  |
| Men's Long Sleeve Pullover Badge Tee Heather      |0          |17                  |
| Toddler Short Sleeve Tee Red                      |12         |17                  |
|Android Men's Long Sleeve Badge Crew Tee Heather   |0          |17                  |
| Men's Airflow 1/4 Zip Pullover Black              |2          |18                  |
| Cam Outdoor Security Camera - CA                  |40         |18                  |
|Women's Weatherblock Shell Jacket Black            |4          |18                  |
| Youth Girl Tee Green                              |9          |19                  |
| RFID Journal                                      |0          |19                  |
| Women's Scoop Neck Tee White                      |52         |19                  |
| Women's Tee Grey                                  |40         |13                  |
|Bottle Opener Clip                                 |381        |10                  |
| Men's Vintage Badge Tee Sage                      |442        |9                   |
| Women's Softshell Jacket Black/Grey               |0          |16                  |
| Women's Long Sleeve Blended Cardigan Charcoal     |37         |18                  |
| Canvas Tote Natural/Navy                          |602        |3                   |
|Android Toddler Short Sleeve T-shirt Pewter        |17         |5                   |
| Women's Short Sleeve Tri-blend Badge Tee Charcoal |88         |5                   |
| Youth Girl Tee Green                              |15         |6                   |
|20 oz Stainless Steel Insulated Tumbler            |0          |8                   |
| Women's Long Sleeve Blended Cardigan Charcoal     |37         |8                   |
| Men's Pullover Hoodie Grey                        |2          |9                   |
| Men's Weatherblock Shell Jacket Black             |0          |10                  |
| Protect Smoke + CO White Wired Alarm-USA          |1361       |13                  |
| Leather Journal-Black                             |0          |15                  |
| Luggage Tag                                       |0          |15                  |
| Men's Short Sleeve Tee                            |6          |16                  |
| Onesie Red/Graphite                               |10         |16                  |
| Women's Quilted Insulated Vest White              |18         |16                  |
| Youth Short Sleeve Tee White                      |31         |19                  |
| Toddler Sports T-shirt Red                        |10         |19                  |
| Women's Short Sleeve Badge Tee Navy               |31         |19                  |
| Pet Feeding Mat                                   |115        |19                  |
|Compact Selfie Stick                               |297        |7                   |
| Water Resistant Bluetooth Speaker                 |205        |6                   |
|7 Dog Frisbee                                      |376        |5                   |
|SPF-15 Slim & Slender Lip Balm                     |4069       |31                  |
| 2200mAh Micro Charger                             |38         |11                  |
| Leatherette Notebook Combo                        |1276       |2                   |
| Men's Short Sleeve Performance Badge Tee Navy     |19         |5                   |
| Onesie Red                                        |2          |5                   |
|Android Women's Short Sleeve Badge Tee Dark Heather|6          |5                   |
| Men's 100% Cotton Short Sleeve Hero Tee Navy      |50         |5                   |
|Android Youth Short Sleeve T-shirt Aqua            |28         |6                   |
| Women's Short Sleeve Tri-blend Badge Tee Charcoal |22         |6                   |
| Women's Shell Jacket Blue/Black                   |7          |6                   |
| Wool Heather Cap Heather/Navy                     |0          |6                   |
|Android Men's Short Sleeve Tri-blend Hero Tee Grey |12         |6                   |
| Youth Girl Tee Green                              |22         |7                   |
|Android Toddler Short Sleeve T-shirt Aqua          |72         |7                   |
| Men's 100% Cotton Short Sleeve Hero Tee Black     |35         |7                   |
|Android Rise 14 oz Mug                             |342        |7                   |
| Youth Short Sleeve Tee White                      |11         |7                   |
|Android Women's Short Sleeve Badge Tee Dark Heather|0          |8                   |
| Toddler Sports T-shirt Red                        |5          |8                   |
| Onesie Red                                        |22         |9                   |
| Spiral Leather Journal                            |449        |9                   |
|Android Women's Short Sleeve Hero Tee Black        |2          |9                   |
| Vintage Henley Grey/Black                         |21         |9                   |
|Android Men's Vintage Tank                         |15         |10                  |
| Women's Convertible Vest-Jacket Sea Foam Green    |0          |10                  |
| Infant Zip Hood Royal Blue                        |29         |10                  |
| Men's Short Sleeve Tee                            |2          |11                  |
| Women's Lightweight Microfleece Jacket            |16         |11                  |
|Yoga Mat Purple                                    |0          |11                  |
| Baby Essentials Set                               |0          |12                  |
| Women's Convertible Vest-Jacket Sea Foam Green    |1          |12                  |
| Women's Short Sleeve Badge Tee Grey               |21         |12                  |
| Men's Fleece Hoodie Black                         |22         |12                  |
| Men's Short Sleeve Performance Badge Tee Black    |11         |12                  |
| Luggage Tag                                       |713        |13                  |
| Women's Scoop Neck Tee Black                      |62         |13                  |
| Onesie Green                                      |21         |13                  |
| Women's Short Sleeve Hero Tee Red Heather         |14         |13                  |
|Gift Card - $50.00                                 |9          |14                  |
|Yoga Block                                         |78         |14                  |
|Android BTTF Cosmos Graphic Tee                    |6          |14                  |
| Toddler 1/4 Zip Fleece Pewter                     |29         |14                  |
| Infant Zip Hood Pink                              |97         |15                  |
| Toddler Short Sleeve Tee White                    |9          |15                  |
| Men's Microfiber 1/4 Zip Pullover Blue/Indigo     |1          |15                  |
| Women's Shell Jacket Blue/Black                   |4          |16                  |
| Women's Performance Hero Tee Gunmetal             |6          |16                  |
| Laptop Backpack                                   |178        |16                  |
| Women's Tee Grey                                  |23         |17                  |
| Women's Long Sleeve Blended Cardigan Charcoal     |9          |17                  |
| Spiral Leather Journal                            |0          |18                  |
| Men's Long & Lean Tee Charcoal                    |0          |18                  |
| Women's Quilted Insulated Vest Black              |1          |18                  |
| Youth Sports Tee Navy                             |33         |18                  |
| Toddler 1/4 Zip Fleece Pewter                     |30         |18                  |
| Onesie Heather                                    |0          |19                  |
|Android Toddler Short Sleeve T-shirt Pink          |22         |19                  |
|Android Men's Vintage Henley                       |27         |19                  |
| Women's Short Sleeve Tri-blend Badge Tee Grey     |8          |19                  |
| Men's Vintage Tank                                |31         |17                  |
| Men's Long & Lean Tee Charcoal                    |43         |12                  |
|Android Men's Take Charge Short Sleeve Tee Purple  |19         |15                  |
| High Capacity 10,400mAh Charger                   |84         |17                  |
| Men's 100% Cotton Short Sleeve Hero Tee Black     |105        |19                  |
| Sunglasses                                        |1195       |5                   |
| Pocket Bluetooth Speaker                          |246        |2                   |
| Men's Short Sleeve Performance Badge Tee Black    |15         |7                   |
|Android Men's Engineer Short Sleeve Tee Charcoal   |55         |11                  |
| Men's Performance 1/4 Zip Pullover Heather/Black  |26         |17                  |
| Women's Typography Short Sleeve Tee               |0          |18                  |
| Collapsible Pet Bowl                              |15         |9                   |
|Sport Bag                                          |2877       |9                   |
| Men's Watershed Full Zip Hoodie Grey              |75         |17                  |
|Android Sticker Sheet Ultra Removable              |449        |13                  |
|Micro Wireless Earbud                              |234        |16                  |
| Women's Performance Hero Tee Gunmetal             |0          |10                  |
| Men's  Zip Hoodie                                 |235        |16                  |
| Women's 1/4 Zip Performance Pullover Two-Tone Blue|15         |19                  |
|22 oz Android Bottle                               |738        |4                   |
|Badge Holder                                       |1186       |2                   |
|Rubber Grip Ballpoint Pen 4 Pack                   |0          |5                   |
| Women's V-Neck Tee Charcoal                       |3          |5                   |
|Android BTTF Moonshot Graphic Tee                  |12         |5                   |
| Men's 100% Cotton Short Sleeve Hero Tee White     |11         |5                   |
| Women's Short Sleeve Hero Tee Heather             |1          |5                   |
| Women's Short Sleeve Hero Tee Heather             |1          |5                   |
| Women's Yoga Jacket Black                         |6          |6                   |
|Android Women's Long Sleeve Blended Cardigan Grey  |0          |6                   |
|BLM Sweatshirt                                     |1          |6                   |
| Women's Vintage Hero Tee Platinum                 |42         |6                   |
|Suitcase Organizer Cubes                           |0          |7                   |
| Men's 100% Cotton Short Sleeve Hero Tee White     |167        |7                   |
| Women's Short Sleeve Performance Tee Pewter       |0          |7                   |
| Women's Convertible Vest-Jacket Sea Foam Green    |11         |8                   |
| Women's Vintage Hero Tee Black                    |155        |8                   |
| Youth Short Sleeve T-shirt Royal Blue             |14         |9                   |
|Gift Card- $100.00                                 |0          |10                  |
|Android Toddler Short Sleeve T-shirt Pink          |70         |11                  |
| Stylus Pen w/ LED Light                           |0          |11                  |
| Women's 1/4 Zip Performance Pullover Two-Tone Blue|1          |11                  |
| Men's Fleece Hoodie Black                         |99         |11                  |
| Men's 100% Cotton Short Sleeve Hero Tee Red       |90         |12                  |
|Android Men's Long & Lean Badge Tee Charcoal       |88         |12                  |
|Android Women's Long Sleeve Blended Cardigan Grey  |10         |12                  |
|Android Lunch Kit                                  |0          |12                  |
| Men's Quilted Insulated Vest Battleship Grey      |3          |12                  |
|Men's Weatherblock Shell Jacket Black              |16         |13                  |
| Women's Vintage Hero Tee Black                    |74         |13                  |
| Men's Vintage Badge Tee Black                     |119        |14                  |
| Women's Long Sleeve Tee Lavender                  |16         |14                  |
| Men's Softshell Jacket Black/Grey                 |0          |14                  |
| Men's Vintage Tank                                |6          |14                  |
| Learning Thermostat 3rd Gen - CA - Stainless Steel|69         |14                  |
| Alpine Style Backpack                             |0          |14                  |
| Pack of 9 Decal Set                               |0          |14                  |
| Youth Baseball Raglan Heather/Black               |7          |14                  |
| Men's Quilted Insulated Vest Battleship Grey      |0          |15                  |
|Android Infant Short Sleeve Tee Pewter             |2          |15                  |
| Insulated Stainless Steel Bottle                  |0          |16                  |
| Women's Quilted Insulated Vest Black              |7          |16                  |
|Women's Weatherblock Shell Jacket Black            |2          |16                  |
|Clip-on Compact Charger                            |0          |16                  |
|Android Men's Vintage Henley                       |2          |16                  |
|Foam Can and Bottle Cooler                         |0          |16                  |
| Men's Vintage Tank                                |1          |17                  |
| Women's Yoga Jacket Black                         |21         |17                  |
| Women's Short Sleeve Hero Tee Charcoal            |5          |17                  |
| Men's Vintage Badge Tee Sage                      |248        |18                  |
| Pack of 9 Decal Set                               |39         |18                  |
| Women's Short Sleeve Hero Tee Grey                |114        |18                  |
| Women's Fleece Hoodie                             |73         |18                  |
| Women's Short Sleeve Performance Tee Charcoal     |0          |18                  |
| Onesie Red/Graphite                               |63         |19                  |
| Youth Baseball Raglan Heather/Black               |0          |19                  |
| Men's Performance 1/4 Zip Pullover Heather/Black  |8          |19                  |
|Android Youth Short Sleeve T-shirt Pewter          |0          |19                  |
| Women's Vintage Hero Tee White                    |37         |19                  |
|Android Men's Vintage Henley                       |10         |19                  |
|Windup Android                                     |1674       |5                   |
| Women's Performance Full Zip Jacket Black         |17         |13                  |
| Device Stand                                      |195        |15                  |
| 25 oz Red Stainless Steel Bottle                  |341        |30                  |
| Toddler Hoodie Royal Blue                         |47         |5                   |
| Men's Short Sleeve Badge Tee Charcoal             |97         |5                   |
|Micro Wireless Earbud                              |0          |5                   |
| Onesie Red/Graphite                               |31         |5                   |
| Women's Scoop Neck Tee White                      |59         |6                   |
| Youth Short Sleeve Tee Red                        |7          |6                   |
| Men's Short Sleeve Performance Badge Tee Charcoal |137        |6                   |
| Mood Happy Window Decal                           |26         |6                   |
| Women's Short Sleeve Hero Tee Grey                |51         |6                   |
| Toddler Short Sleeve T-shirt Royal Blue           |30         |6                   |
| Lunch Bag                                         |0          |6                   |
| Onesie Red/Graphite                               |6          |7                   |
| Men's Short Sleeve Performance Badge Tee Pewter   |107        |7                   |
|Android Youth Short Sleeve T-shirt Aqua            |77         |7                   |
|Android Lifted Men's Short Sleeve Tee Blue         |9          |7                   |
| Men's 100% Cotton Short Sleeve Hero Tee Navy      |0          |7                   |
| Toddler Hoodie Royal Blue                         |51         |7                   |
|Android Toddler Short Sleeve T-shirt Pewter        |4          |8                   |
| Women's Short Sleeve Hero Tee Charcoal            |4          |8                   |
| Men's Short Sleeve Badge Tee Charcoal             |48         |8                   |
| Women's Short Sleeve Tri-blend Badge Tee Grey     |4          |8                   |
| Women's Short Sleeve Badge Tee Navy               |33         |8                   |
| Men's Airflow 1/4 Zip Pullover Lapis              |6          |8                   |
| Men's Watershed Full Zip Hoodie Grey              |54         |9                   |
| Men's Microfiber 1/4 Zip Pullover Blue/Indigo     |9          |9                   |
|Men's Softshell Jacket Black/Grey                  |3          |9                   |
|Android Men's Engineer Short Sleeve Tee Charcoal   |13         |9                   |
| Women's Vintage Hero Tee Black                    |121        |9                   |
|26 oz Double Wall Insulated Bottle                 |256        |9                   |
| Men's Performance Full Zip Jacket Black           |0          |9                   |
| Men's Colorblock Tee White/Heather                |6          |10                  |
| Baby Essentials Set                               |194        |10                  |
| Men's Long & Lean Tee Charcoal                    |33         |10                  |
| Leather Journal-Black                             |354        |10                  |
|Android Men's Engineer Short Sleeve Tee Charcoal   |26         |11                  |
| Onesie Heather                                    |71         |11                  |
|BLM Sweatshirt                                     |9          |11                  |
|Android Men's Paradise Short Sleeve Tee Olive      |3          |11                  |
| Onesie Green                                      |50         |11                  |
|Android Men's Short Sleeve Hero Tee Heather        |57         |12                  |
|Android Men's Paradise Short Sleeve Tee Olive      |18         |12                  |
|Android BTTF Cosmos Graphic Tee                    |10         |12                  |
| Men's Microfiber 1/4 Zip Pullover Blue/Indigo     |3          |12                  |
| Toddler Short Sleeve Tee White                    |12         |12                  |
| Hard Cover Journal                                |2046       |13                  |
|8 pc Android Sticker Sheet                         |0          |13                  |
| Women's Short Sleeve Hero Tee Heather             |3          |13                  |
| RFID Journal                                      |2839       |13                  |
| Women's Tee Grey                                  |0          |13                  |
| Toddler Short Sleeve Tee White                    |18         |13                  |
|Android Women's Fleece Hoodie                      |18         |14                  |
| Men's Quilted Insulated Vest Black                |18         |14                  |
| Mood Ninja Window Decal                           |0          |14                  |
|Android Men's Engineer Short Sleeve Tee Charcoal   |4          |14                  |
| Flashlight                                        |0          |14                  |
| Men's Short Sleeve Performance Badge Tee Charcoal |43         |15                  |
| Men's Quilted Insulated Vest Battleship Grey      |9          |15                  |
|Android Men's Vintage Tank                         |64         |15                  |
| Collapsible Pet Bowl                              |59         |15                  |
| Men's Airflow 1/4 Zip Pullover Black              |7          |16                  |
|Women's  Short Sleeve Hero Tee Black               |6          |16                  |
|Android Men's Short Sleeve Tri-blend Hero Tee Grey |12         |16                  |
| Youth Short Sleeve Tee Red                        |4          |17                  |
| Women's Short Sleeve Tri-blend Badge Tee Charcoal |89         |18                  |
|Android Hard Cover Journal                         |0          |18                  |
| Men's Vintage Tank                                |1          |18                  |
|Waterproof Backpack                                |0          |18                  |
|Android BTTF Moonshot Graphic Tee                  |20         |19                  |
|Android Toddler Short Sleeve T-shirt Pink          |70         |19                  |
|Android Men's Vintage Tank                         |23         |19                  |
| Men's Long & Lean Tee Charcoal                    |251        |19                  |
| Toddler Hoodie Royal Blue                         |41         |19                  |
|Yoga Mat                                           |0          |19                  |
| Infant Zip Hood Royal Blue                        |108        |19                  |
| Men's Fleece Hoodie Black                         |20         |19                  |
|Basecamp Explorer Powerbank Flashlight             |306        |14                  |
| Screen Cleaning Cloth                             |1324       |5                   |
| Flashlight                                        |13         |6                   |
| Women's Quilted Insulated Vest Black              |10         |11                  |
| Men's Long & Lean Tee Charcoal                    |11         |14                  |
| Women's Vintage Hero Tee White                    |172        |14                  |
| Men's Colorblock Tee White/Heather                |1          |8                   |
|Android Lunch Kit                                  |163        |12                  |
|1 oz Hand Sanitizer                                |679        |3                   |
| Women's Vintage Hero Tee Platinum                 |34         |5                   |
| Women's Short Sleeve Hero Tee Red Heather         |16         |6                   |
| Women's 1/4 Zip Performance Pullover Black        |21         |12                  |
| Men's Performance Hero Tee Gunmetal               |1          |17                  |
| Men's Fleece Hoodie Black                         |142        |17                  |
|Gunmetal Roller Ball Pen                           |1321       |36                  |
| 22 oz Water Bottle                                |15607      |2                   |
| Toddler Short Sleeve Tee White                    |12         |5                   |
|25L Classic Rucksack                               |0          |5                   |
|Android Toddler Short Sleeve T-shirt Pink          |0          |5                   |
| Men's Vintage Tank                                |41         |5                   |
| Men's 100% Cotton Short Sleeve Hero Tee Black     |0          |5                   |
| Men's Convertible Vest-Jacket Pewter              |8          |5                   |
|Android Twill Cap                                  |161        |5                   |
|Windup Android                                     |0          |6                   |
| Bib White                                         |116        |6                   |
|Android Infant Short Sleeve Tee Pewter             |8          |6                   |
| Women's Scoop Neck Tee Black                      |23         |7                   |
| Protect Smoke + CO White Battery Alarm-USA        |0          |7                   |
|Red Spiral  Notebook                               |43         |8                   |
| Men's Performance Hero Tee Gunmetal               |10         |8                   |
|Android Men's Long Sleeve Badge Crew Tee Heather   |92         |8                   |
|Ballpoint Pen Blue                                 |400        |8                   |
|Android Men's Take Charge Short Sleeve Tee Purple  |68         |8                   |
| Infant Short Sleeve Tee White                     |7          |8                   |
| Women's Long Sleeve Blended Cardigan Charcoal     |0          |8                   |
| Men's Airflow 1/4 Zip Pullover Black              |41         |9                   |
| Men's Pullover Hoodie Grey                        |0          |9                   |
| Youth Short Sleeve Tee White                      |3          |9                   |
| Women's Short Sleeve Hero Tee Black               |0          |9                   |
|Android Youth Short Sleeve T-shirt Pewter          |3          |10                  |
|Gift Card - $250.00                                |38         |10                  |
|Android Men's  Zip Hoodie                          |14         |10                  |
| Men's Performance 1/4 Zip Pullover Heather/Black  |18         |11                  |
|Android Men's  Zip Hoodie                          |0          |11                  |
|Android Men's Pep Rally Short Sleeve Tee Navy      |41         |11                  |
| Women's Short Sleeve Hero Tee White               |0          |12                  |
|23 oz Wide Mouth Sport Bottle                      |142        |12                  |
|Waterproof Gear Bag                                |0          |12                  |
| Women's Short Sleeve Hero Tee White               |51         |12                  |
| Men's Bayside Graphic Tee                         |7          |13                  |
| Men's Airflow 1/4 Zip Pullover Black              |7          |14                  |
| Men's  Zip Hoodie                                 |15         |14                  |
| Men's Microfiber 1/4 Zip Pullover Blue/Indigo     |16         |14                  |
| Men's Vintage Badge Tee Black                     |395        |14                  |
| Youth Short Sleeve T-shirt Yellow                 |59         |14                  |
| Men's Long & Lean Tee Grey                        |0          |15                  |
| Women's Convertible Vest-Jacket Black             |5          |15                  |
| Trucker Hat                                       |0          |15                  |
| Women's Convertible Vest-Jacket Black             |15         |15                  |
| Men's Long & Lean Tee Charcoal                    |295        |15                  |
| Womens 3/4 Sleeve Baseball Raglan Heather/Black   |33         |15                  |
|Android Men's Vintage Henley                       |43         |15                  |
| Men's Long Sleeve Raglan Ocean Blue               |70         |15                  |
|Women's Performance Full Zip Jacket Black          |7          |16                  |
| Men's 100% Cotton Short Sleeve Hero Tee Navy      |37         |16                  |
| Youth Baseball Raglan Heather/Black               |21         |16                  |
|25L Classic Rucksack                               |40         |16                  |
| Men's Short Sleeve Badge Tee Charcoal             |9          |16                  |
| Infant Zip Hood Royal Blue                        |62         |16                  |
| Men's Long & Lean Tee Charcoal                    |102        |17                  |
| Toddler Short Sleeve Tee Red                      |7          |17                  |
| Women's Short Sleeve Hero Tee Black               |37         |17                  |
| Toddler Short Sleeve Tee Red                      |71         |18                  |
| Men's Bayside Graphic Tee                         |21         |18                  |
| Women's 1/4 Zip Performance Pullover Black        |8          |19                  |
| Men's Short Sleeve Hero Tee Light Blue            |35         |19                  |
| Women's 1/4 Zip Performance Pullover Black        |7          |19                  |
| Lunch Bag                                         |290        |11                  |
| Sunglasses                                        |2444       |13                  |
| Women's Quilted Insulated Vest White              |16         |9                   |
| Men's Quilted Insulated Vest Battleship Grey      |45         |11                  |
| Women's Scoop Neck Tee White                      |81         |18                  |
|Leatherette Journal                                |4978       |36                  |
| Sunglasses                                        |6805       |5                   |
| Doodle Decal                                      |2080       |5                   |
| Women's Tee Grey                                  |11         |5                   |
| Doodle Decal                                      |0          |7                   |
|26 oz Double Wall Insulated Bottle                 |0          |8                   |
| Women's Vintage Hero Tee Lavender                 |4          |8                   |
|Sport Bag                                          |0          |8                   |
| Women's Convertible Vest-Jacket Black             |25         |8                   |
|UpCycled Bike Saddle Bag                           |0          |8                   |
| Men's Vintage Henley                              |59         |8                   |
| Women's Typography Short Sleeve Tee               |0          |9                   |
| Onesie Heather                                    |21         |10                  |
| Men's 100% Cotton Short Sleeve Hero Tee Black     |1101       |10                  |
|Android Men's  Zip Hoodie                          |12         |11                  |
|Collapsible Shopping Bag                           |117        |11                  |
| Youth Sports Tee Navy                             |0          |12                  |
|1 oz Hand Sanitizer                                |0          |12                  |
|Android Stretch Fit Hat M/L                        |59         |13                  |
| Infant Short Sleeve Tee Red                       |4          |13                  |
|Android Infant Short Sleeve Tee Pink               |9          |14                  |
|Plastic Sliding Flashlight                         |2561       |14                  |
| Women's Performance Golf Polo Blue                |3          |14                  |
| Men's Bayside Graphic Tee                         |25         |15                  |
|Android 5-Panel Low Cap                            |11         |16                  |
| Women's 1/4 Zip Performance Pullover Two-Tone Blue|8          |16                  |
|24 oz  Sergeant Stripe Bottle                      |0          |17                  |
| Women's Vintage Hero Tee Lavender                 |43         |17                  |
| Men's Fleece Hoodie Black                         |175        |17                  |
|Android Hard Cover Journal                         |102        |17                  |
| Men's Long Sleeve Raglan Ocean Blue               |9          |18                  |
| Toddler Hoodie Royal Blue                         |0          |18                  |
| Men's Long & Lean Tee Grey                        |22         |18                  |
|BLM Sweatshirt                                     |4          |18                  |
|Android Women's Short Sleeve Badge Tee Dark Heather|4          |19                  |
|Android Toddler Short Sleeve T-shirt Pink          |19         |19                  |
| Women's Yoga Pants                                |3          |6                   |
| Women's Short Sleeve Performance Tee Pewter       |44         |5                   |
| Men's Bike Short Sleeve Tee Charcoal              |129        |5                   |
| Men's Airflow 1/4 Zip Pullover Lapis              |3          |5                   |
| Women's Long Sleeve Blended Cardigan Charcoal     |14         |5                   |
| Onesie Green                                      |110        |5                   |
| Rucksack                                          |0          |5                   |
| Men's Short Sleeve Hero Tee Charcoal              |98         |5                   |
| Men's Long & Lean Tee Charcoal                    |85         |5                   |
| Stretch Fit Hat M/L Navy                          |6          |6                   |
| Baby Essentials Set                               |349        |6                   |
| Youth Sports Tee Navy                             |48         |6                   |
| Infant Zip Hood Pink                              |147        |6                   |
|Men's Weatherblock Shell Jacket Black              |44         |7                   |
| Women's Short Sleeve Hero Tee Sky Blue            |24         |7                   |
| Women's Vintage Hero Tee Platinum                 |6          |8                   |
| Leather Journal-Brown                             |451        |9                   |
| Men's Airflow 1/4 Zip Pullover Black              |0          |9                   |
|Gift Card - $25.00                                 |107        |10                  |
| Men's Short Sleeve Hero Tee White                 |32         |10                  |
| Men's Short Sleeve Hero Tee Light Blue            |26         |10                  |
| Men's 100% Cotton Short Sleeve Hero Tee Red       |34         |10                  |
| Men's Performance 1/4 Zip Pullover Heather/Black  |6          |11                  |
| Baby on Board Window Decal                        |415        |11                  |
| Learning Thermostat 3rd Gen-USA - White           |0          |11                  |
| Men's Short Sleeve Hero Tee Charcoal              |18         |12                  |
| Alpine Style Backpack                             |272        |12                  |
| Men's 100% Cotton Short Sleeve Hero Tee Black     |148        |12                  |
| Men's Short Sleeve Hero Tee Charcoal              |0          |12                  |
| Youth Baseball Raglan Heather/Black               |28         |13                  |
| Onesie Heather                                    |43         |14                  |
|Android Men's Paradise Short Sleeve Tee Olive      |30         |14                  |
| Men's Long & Lean Tee Grey                        |81         |14                  |
| Bib Red                                           |44         |15                  |
|Android Lifted Men's Short Sleeve Tee Blue         |4          |16                  |
| Youth Girl Tee Green                              |18         |16                  |
|Android Lifted Men's Short Sleeve Tee Blue         |11         |16                  |
| Men's Vintage Henley                              |0          |17                  |
|BLM Sweatshirt                                     |1          |17                  |
| Men's Long & Lean Tee Grey                        |26         |17                  |
| Men's Short Sleeve Hero Tee Black                 |21         |18                  |
| Men's Long Sleeve Raglan Ocean Blue               |0          |18                  |
|Android Youth Short Sleeve T-shirt Aqua            |39         |18                  |
| Men's Long Sleeve Raglan Ocean Blue               |71         |18                  |
| Infant Short Sleeve Tee White                     |55         |19                  |
| Infant Short Sleeve Tee Red                       |18         |19                  |
| Women's 1/4 Zip Jacket Charcoal                   |7          |18                  |
| Men's 100% Cotton Short Sleeve Hero Tee Navy      |29         |6                   |
|Android Men's Vintage Tank                         |57         |10                  |
| Men's 100% Cotton Short Sleeve Hero Tee White     |749        |12                  |
| Women's Long Sleeve Tee Lavender                  |128        |13                  |
| Women's Fleece Hoodie                             |78         |15                  |
| Women's Short Sleeve Hero Tee Black               |121        |16                  |
|Android Men's  Zip Hoodie                          |17         |16                  |
| Women's Short Sleeve Performance Tee Charcoal     |18         |11                  |
| Women's Shell Jacket Blue/Black                   |5          |7                   |
| Executive Umbrella                                |458        |5                   |
|7 Dog Frisbee                                      |324        |5                   |
| Mobile Phone Vent Mount                           |129        |15                  |
| Device Holder Sticky Pad                          |94         |8                   |
| Women's Short Sleeve Badge Tee Grey               |8          |8                   |
| Women's Weatherblock Shell Jacket Black           |1          |13                  |
|Android Men's Paradise Short Sleeve Tee Olive      |0          |14                  |
|Seat Pack Organizer                                |304        |11                  |
| Twill Cap                                         |1755       |5                   |
| Toddler Short Sleeve T-shirt Grey                 |123        |5                   |
| Women's Quilted Insulated Vest White              |5          |5                   |
|Android Youth Short Sleeve T-shirt Pewter          |5          |5                   |
| Infant Zip Hood Royal Blue                        |0          |6                   |
| Women's Convertible Vest-Jacket Sea Foam Green    |19         |6                   |
| Men's Short Sleeve Hero Tee Light Blue            |17         |6                   |
| Tote Bag                                          |0          |6                   |
|Android Men's Vintage Henley                       |19         |6                   |
| Vintage Henley Grey/Black                         |30         |6                   |
| Men's  Zip Hoodie                                 |98         |6                   |
|Android Youth Short Sleeve T-shirt Pewter          |5          |7                   |
| Leather Perforated Journal                        |0          |7                   |
| Laptop Backpack                                   |0          |7                   |
| 4400mAh Power Bank                                |0          |7                   |
| Men's 100% Cotton Short Sleeve Hero Tee Red       |29         |8                   |
|Android Stretch Fit Hat                            |34         |8                   |
|Android Men's Long Sleeve Badge Crew Tee Heather   |28         |9                   |
| Zipper-front Sports Bag                           |307        |9                   |
|Android Spiral Journal with Pen                    |1280       |9                   |
| Youth Short Sleeve T-shirt Green                  |32         |9                   |
|Android RFID Journal                               |0          |9                   |
| Leather Journal                                   |0          |9                   |
| Men's Long Sleeve Raglan Ocean Blue               |125        |10                  |
|Android Men's Take Charge Short Sleeve Tee Purple  |44         |10                  |
| Men's  Zip Hoodie                                 |41         |10                  |
| Men's Vintage Henley                              |87         |10                  |
| Toddler Short Sleeve Tee White                    |40         |10                  |
| Toddler Raglan Shirt Blue Heather/Navy            |22         |10                  |
| Youth Short Sleeve T-shirt Green                  |7          |11                  |
| Women's Short Sleeve Hero Tee Black               |252        |11                  |
| Women's Quilted Insulated Vest Black              |1          |12                  |
| Women's Typography Short Sleeve Tee               |0          |12                  |
|Android Men's Long Sleeve Badge Crew Tee Heather   |95         |13                  |
| 17oz Stainless Steel Sport Bottle                 |1390       |13                  |
|Android Men's Long & Lean Badge Tee Charcoal       |129        |13                  |
| Leather Perforated Journal                        |1305       |13                  |
| Onesie Red                                        |5          |13                  |
| Women's Short Sleeve Tri-blend Badge Tee Grey     |3          |13                  |
| Infant Short Sleeve Tee White                     |30         |13                  |
| Toddler Raglan Shirt Blue Heather/Navy            |9          |14                  |
| Youth Girl Hoodie                                 |7          |14                  |
|Android Women's Short Sleeve Hero Tee Black        |5          |14                  |
| Men's 100% Cotton Short Sleeve Hero Tee Red       |92         |14                  |
| Men's Vintage Badge Tee White                     |76         |14                  |
| Men's Fleece Hoodie Black                         |143        |14                  |
| High Capacity 10,400mAh Charger                   |0          |14                  |
| Women's Long Sleeve Tee Lavender                  |0          |15                  |
| Men's Short Sleeve Hero Tee Light Blue            |0          |15                  |
| Men's Microfiber 1/4 Zip Pullover Blue/Indigo     |3          |15                  |
| Protect Smoke + CO White Wired Alarm - CA         |49         |15                  |
| Men's Airflow 1/4 Zip Pullover Black              |41         |15                  |
| Women's Lightweight Microfleece Jacket            |3          |15                  |
| Infant Short Sleeve Tee Royal Blue                |9          |16                  |
| Women's Short Sleeve Hero Tee Grey                |138        |16                  |
| Women's Short Sleeve Performance Tee Charcoal     |11         |16                  |
| Women's Short Sleeve Hero Tee Red Heather         |13         |17                  |
|Android Men's Short Sleeve Hero Tee Heather        |193        |18                  |
| Infant Short Sleeve Tee Royal Blue                |7          |18                  |
| Women's Short Sleeve Badge Tee Grey               |21         |18                  |
| Infant Short Sleeve Tee Red                       |15         |18                  |
| Cam Outdoor Security Camera - USA                 |0          |18                  |
|25L Classic Rucksack                               |0          |19                  |
| Cam Indoor Security Camera - CA                   |72         |19                  |
|Android Stretch Fit Hat Black                      |52         |19                  |
| Women's Performance Hero Tee Gunmetal             |5          |19                  |
| 22 oz Water Bottle                                |19678      |4                   |
| Onesie Heather                                    |37         |6                   |
| Men's Airflow 1/4 Zip Pullover Lapis              |0          |8                   |
| Men's Quilted Insulated Vest Black                |0          |9                   |
| Men's  Zip Hoodie                                 |41         |12                  |
|Android Women's Long Sleeve Blended Cardigan Grey  |58         |12                  |
|Android BTTF Cosmos Graphic Tee                    |5          |13                  |
| Men's Bayside Graphic Tee                         |3          |14                  |
| Hard Cover Journal                                |2171       |14                  |
| Youth Short Sleeve Tee Red                        |31         |14                  |
|Android Men's Short Sleeve Hero Tee White          |95         |15                  |
| Youth Short Sleeve T-shirt Yellow                 |51         |15                  |
| Womens 3/4 Sleeve Baseball Raglan Heather/Black   |25         |15                  |
| Men's Short Sleeve Performance Badge Tee Pewter   |25         |16                  |
|25L Classic Rucksack                               |0          |16                  |
| Onesie Green                                      |0          |17                  |
| Women's Short Sleeve Hero Tee Charcoal            |21         |17                  |
| Women's Convertible Vest-Jacket Sea Foam Green    |25         |8                   |
| Women's Convertible Vest-Jacket Black             |48         |10                  |
|Android Women's Short Sleeve Hero Tee Black        |11         |7                   |
| Men's Bike Short Sleeve Tee Charcoal              |12         |7                   |
| Men's 100% Cotton Short Sleeve Hero Tee Red       |72         |8                   |
| Women's Short Sleeve Performance Tee Pewter       |1          |9                   |
| Men's Typography Short Sleeve Tee                 |1          |11                  |
| Men's Softshell Jacket Black/Grey                 |1          |12                  |
| Men's Vintage Tank                                |119        |15                  |
| Women's Fleece Hoodie Black                       |5          |17                  |
|Android Men's Long Sleeve Badge Crew Tee Heather   |87         |13                  |




Question 3: Show unique page title from all sessions and time spent on site?

SQL Queries: 
SELECT  DISTINCT(page_title), Coalesce(To_Timestamp(time_on_site)) time FROM all_sessions
WHERE page_title IS NOT NULL AND time_on_site IS NOT NULL
ORDER by time 
limit 10


Answer: 
This shows the time visited on each page title from all_sessions

sample size of 10

RESULTS

|page_title                                         |time |
|---------------------------------------------------|-----|
|Google &#124; Shop by Brand &#124; Google Merchandise Store  |1969-12-31 18:00:01-06|
|YouTube &#124; Shop by Brand &#124; Google Merchandise Store |1969-12-31 18:00:01-06|
|The Google Merchandise Store/Google G Noise-reducing Bluetooth Headphones|1969-12-31 18:00:01-06|
|YouTube Custom Decals                              |1969-12-31 18:00:01-06|
|Women's T-Shirts &#124; Apparel &#124; Google Merchandise Store|1969-12-31 18:00:01-06|
|Electronics &#124; Google Merchandise Store             |1969-12-31 18:00:01-06|
|Electronics                                        |1969-12-31 18:00:01-06|
|Office                                             |1969-12-31 18:00:01-06|
|Women's T-Shirts &#124; Apparel &#124; Google Merchandise Store|1969-12-31 18:00:02-06|
|Electronics &#124; Google Merchandise Store             |1969-12-31 18:00:02-06|







Question 4: 

SQL Queries:

Answer:



Question 5: 

SQL Queries:

Answer:
