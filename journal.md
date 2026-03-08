# Journal of the Design and eventual Build Process of my high-performance custom hotend, Double Barrel. 
### Parker Rupe
### Total Hours: 


## Journal Entry 1: 3/1/2026
Time Spent: 6 Hours

Okay. So, this will be my first custom hotend design that I actually finish, but not my first custom hotend design. I actually started designing one in the past for Quantumania which utilized four supervolcano heaters. However, I have decided I honestly don't really like it. 4 heaters feels like a bit much and keeping it at 24v introduces a lot of nastiness when it comes to breakout boards and whatnot due to absurd amperage. 
So, after a bit of digging on AliExpress (half an hour D:) I found some 6x80mm 120w mains heater cartridges that should be pretty perfect. Of course, I will use two of them, for sillies. I almost used three but I didn't want to copy tricorn or 1Mon's custom hotend. I even considered 4, like the original hotend, but... that would be able to melt a block in literal seconds. In theory two could do that too, but theres no need to go so absurdly overboard.
I actually have a plan for protecting myself in event of mosfet failure that I will detail later. 
https://www.aliexpress.us/item/3256802953795845.html
These are the heaters. For some reason I can't buy less than 10 for cheaper? It is what it is. 
Anyways, I started off by making a quick sketch to outline spacing between the heaters and meltzone. 

<img width="952" height="694" alt="image" src="https://github.com/user-attachments/assets/0e0e547f-9e01-41ae-bd68-caab50c57f7f" />

It's kind of a mess but it is what it is tbh. Most importantly, it's functional. 
That then gets extruded 80mm, as that is what I want for my hot side length. Match the heaters. 

<img width="816" height="1026" alt="image" src="https://github.com/user-attachments/assets/a6ccba30-c79b-4668-9bb1-b82fcda67430" />

From there I sketch and extrude a top/bottom so that I have enough material for mounting, heater retaining, etc. 

<img width="756" height="1026" alt="image" src="https://github.com/user-attachments/assets/9bd93f3b-81ed-47d8-980d-f26997edf19b" />

Next comes fillets and mounting holes. The ones to the side are heater setscrews (on the barrels if you will... double barrel... double heater... anyways). The ones on the center flat part are for M3 stud thermistors. I LOVE M3 thermistors. I use them on everything. So handy. 

<img width="641" height="1077" alt="image" src="https://github.com/user-attachments/assets/7ffd8241-c78c-4406-b08a-5c6f3c5fa8e0" />

That took about an hour and a half as I had to change it a few times to make spacing realistic and whatnot. I also had a lot of issues with the fillets for some reason? Fusion is weird sometimes.

I'm gonna skip ahead about 3-4 hours because going step by step is a really boring read. In order I:
Inserted the heatbreak and nozzle
Designed a basic heat sink
Added heat sink bracing

<img width="539" height="1005" alt="image" src="https://github.com/user-attachments/assets/0a8544a5-af4e-48dd-8e6b-8e59c7353a51" />

<img width="519" height="1091" alt="image" src="https://github.com/user-attachments/assets/7da8281b-f7e3-4b8f-a977-9bb737738b57" />

The heat break is some cheapo mellow one that I was using for my old hot end design - I don't have the link right now but I will add it next entry!. The heatsink is quite simple, copying the fin style/count of the TZ E3 heatsink because I know that configuration works and I am not really space or mounting constrained. I don't really have mounting yet actually but... it will happen.
The braces are 1mm lasercut titanium. Titanium is a really bad heat conductor, and the struts are thin, so it won't conduct much heat at all into the heatsink. It is kinda funny to brace it up here considering the sheer cantilever of mass with the brutal length of the hotend... but I am NOT snapping a heatbreak again. 
All the hardware for this fella will be M3 or M2. M2 on the cold side, M3 on the hot side. Super simple. 

<img width="519" height="1091" alt="image" src="https://github.com/user-attachments/assets/e812586e-b1a3-4a89-a981-1903373d7692" />

The heat sink was made with a simple projected sketch and pattern. I created a seperate cylindrical core so I didn't have to worry about preserving it for making the fins and then just combined all the bodies (fins and cylinder core) into the one heat sink.
That's all for today. Next I need to work on adding hardware, budget planning, machineability optimization, and part sourcing. 
