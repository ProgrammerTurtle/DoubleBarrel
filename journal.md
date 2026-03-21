<img width="1548" height="3811" alt="doublebarrelhotendnobg" src="https://github.com/user-attachments/assets/3217bc88-5a6c-4738-b30e-4b683ab4f228" /># Journal of the Design and eventual Build Process of my high-performance custom hotend, Double Barrel. 
### Parker Rupe
### Total Hours: 19.5


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


## Journal Entry 2: 3/8/2026
Time Spent: 4.5 hours

Uhhh. So JLC told me that they won't do a 67mm long 2mm diameter hole in my heatblock. Crazy !! So... I have to figure out a meltzone adapter. Because they can do an M6 hole apparently! 
Spoiler alert... I spent 3 hours searching for options that could work or ways to get one custom made. Ugh. 
First things first I threw together a quick model and drawing of the part I need. The point of the drawing will be clear soon. 

<img width="1766" height="406" alt="image" src="https://github.com/user-attachments/assets/0fb8af26-2427-4621-9f3a-3e7edb67ee65" />

By the way. This drawing is abhorrent. My engineering friend yelled at me when he saw it and said it hurt him. But it gets the point across. 

<img width="402" height="1054" alt="image" src="https://github.com/user-attachments/assets/ede7b168-2191-4656-9e9b-2b1a57b0d257" />
<img width="378" height="1011" alt="image" src="https://github.com/user-attachments/assets/18ee6b8a-d403-4cae-9d24-71ef1eff7b3d" />

Basically it is a 67mm (shut up) long M6 threaded rod with a 2mm throughbore and an M2 hex drive on the end. These exist for supervolcano and volcano hotends to allow for normal v6 nozzle useage in long blocks.
This brings us to the first few options. I can adjsut the length of the block slightly (a little shorter or a little longer) to allow for stacking up 2 supervolcano adapters or 1 supervolcano adapter and 3-4 volcano adapters. The first option results in a 100mm ish meltzone... which is literally the max z print height of Quantumania... uhhhhh... Yeah I don't want to do that. The second option is just flat out silly. It would work better, but man is it a lot of possible leak/fail points. And it makes assembly super annoying as you have to heat tighten all 4 or 5 inserts. 
So after researching those available inserts and doing the math for all the combo possibilities... I decided that I don't want to do that. So, I emailed Misumi. 

I have utilized Misumi before for custom linear shafts, for a combat robot weapon assembly. They allow you to customize it in a lot of ways and it is super affordable! But, they don't have a way to do a hex drive, nor fully threaded (it needs like 2mm of not threaded due to configurator weirdness). I decided to see if it could be done through their "fully threaded stud/bolt" item. This got quite close too! But unfortunately, there is not an option for a through bore. So, I sent them an email, with the drawing/sketch from earlier, basically asking if they had a way to do this part that I was missing. I think they do have a way, I just can't find it, despite spending 2 and a half hours on their site. I waited "on hold" with their chat bot for a while before it eventually said support was not active right now and to send an email. It is like 6:30 AM on a sunday but still I wanted to try.
Besides that, I will probably try to quote one from JLC if misumi says they cannot do it or if it is too expensive. Which means I need to actually make a proper drawing and I don't know if they can do hex broaching so this might get some weird drive socket. 

That genuinely took way longer than I thought it would. But that's ok. TL;DR, need to use an M6 threaded meltzone, like Chube, and tried to figure out sourcing a custom one. 

## Journal Entry 3: 3/15/2026
Time Spent: 4 hours

Okay, today was pretty much finishing touches for submission. I added some mounting options and made mechanical drawings so I can request proper quotes from JLCCNC for BOM pricing. 

For mounting, I have both a 4 hole top mounting option and a 2 hole side mounting option. This allows for flexibility in mounting. I don't need to worry a ton about how rigid it is because I need to brace at the bottom of the hotend either way. Not saying these won't be rigid, but it is less of an issue. This took about half an hour as I had to go through my various printers and see what mounting options would fit as I want flexibility and versatility. 

I ended up going with: 

<img src="https://user-cdn.hackclub-assets.com/019cf047-dda4-7c05-a758-1147a216067c/Screenshot%202026-03-15%20005530.png" />

This 4 hole mounting up top, which is a 4 hole M3 5.5 x 10mm pattern. This allows a bowden tube/connector to fit. 

<img src="https://cdn.hackclub.com/019cf047-dda4-7c05-a758-1147a216067c/Screenshot%202026-03-15%20005530.png" />

This is the second mounting option, with a matching hole on the opposite side. This is also M3. This option will not be stable without bracing on the end of the hotend. The other option I feel needs end bracing for performance aswell, but technically it is optional. 

As for finishing touches, I just went through and toleranced everything, made my holes have cone ends so they can be drilled properly, etc. 
I also made drawings! Here are those. 

<img src="https://cdn.hackclub.com/019cf06f-8032-7efa-a67f-9113b47da0f9/Screenshot%202026-03-15%20013903.png" />

This is the heatsink drawing, which calls out all major dimensions and more importantly threaded holes for the heatsink. A little bit messy but very usable and one of my better drawings. This took an hour and a half. 

<img src="https://cdn.hackclub.com/019cf07d-c142-70df-b5b1-6b4c7f4694bc/Screenshot%202026-03-15%20015440.png" /> 

And this is the heater block drawing. This was a little difficult as it was smoothing out the edges of the center flat section, making the part drawings weird as they lacked those center lines. I made it work though, hopefully JLC likes it. 

That took the remaining 3.5 hours of this session, besides submitting for a quote of course. I hate making drawings and need to practice so that is the main reason why it took a hot minute - I had to do some research on proper procedure for calling out threads and whatnot. 
Once I get the quotes back on Monday, I will submit this project! 

## Journal Entry 4: 3/18/2026
Time Spent: 3 hours

Hi gang. Gonna be a bit more informal with this one because formality gets a bit boring sometimes. 
So, I got the quotes back. 

<img width="909" height="340" alt="image" src="https://github.com/user-attachments/assets/c390c659-d55d-4f8a-9f48-63f0b8fb8f59" />

I submitted them and soon got an email saying there was an issue. I panicked. I thought they wouldn't be able to machine my heaterblock because of the stupid 80mm long M6 tapped hole. But! The issue was just something with shipping. After I fixed that it actually passed review with no errors. I am amazed. 
It's a bit expensive though, especially the heatsink, which costs more than the heaterblock somehow. This means I will have to resort to getting the heatsink SLM'd by In3DTec out of aluminum. I also made some changes to the heaterblock that I will show here, but basicallly I just nuked the fillets to save money. I also figured out what I will do for the melt zone adapter - I will be buying two supervolcano adapters and cutting one down to size. 

<img width="563" height="996" alt="image" src="https://github.com/user-attachments/assets/0a9d8f93-6120-4e4f-be08-e426c33ebef4" />

Here's the mew block. Much simpler but still retains the look I was going for. I actually like the chamfers more than the fillets. I had to make some changes to the mechanical drawing aswell to account for the new model and highlight the absurd 80mm long M6 tapped hole, but those changes are not super large so I don't think I will put screenshots. But, they will be uploaded to the repo. 

<img width="510" height="1032" alt="image" src="https://github.com/user-attachments/assets/130c8181-95ba-4229-ac62-d0487fcb86ca" />

That makes this the hotend now, minus screws. Looks pretty cool! 
Once JLC responds to my new quote, which should happen tonight, I can actually submit this thing. In the meantime, I started finding aliexpress stuff for my BOM. We have: 
Heaters: https://www.aliexpress.us/item/3256802953795845.html
Supervolcano Adapters: https://www.aliexpress.us/item/3256805546562989.html

<img width="1437" height="853" alt="image" src="https://github.com/user-attachments/assets/9eaf1fc0-37cd-4b27-b071-6b02a581d10b" />

This is the In3DTec quote for the heatsink, which is a great price. I just have to tap it myself because I don't want to deal with their tapping stuff, but thats fine.

I also need to get quotes for the heatbreak braces. I plan on getting them made by JLC out of 1mm stainless steel, as steel is a poor thermal conductor (and a dissimilar metal from aluminum which helps even more). I have to wait until midnight GMT+8 (10am my time) to submit that quote though as they are running the sheet metal service at very low capacity, and today's capacity is full. 

That's basically it. Optimizing stuff for the correct prices and adjusting my drawings to account for the manufacturability changes took a while. Fusion is also a bit goofy when it comes to chamfers/fillets so I had to deal with that. 
With any luck, I can submit tomorrow. 

## Journal Entry 5: 3/19/2026
Time Spent: 2 hours

Okay, I missed the window to quote the braces. Whoops. I will try again tomorrow. As for today, I put the finishing touches on the 3D model, wrote most of the BOM, and worked on formatting my repo. 

I basically just added all the hardware and made colors/materials correct. I modeled M3 stud thermistors and the 80mm heaters myself. 

<img width="486" height="897" alt="image" src="https://github.com/user-attachments/assets/796b7b46-e7cf-488c-960b-67d80cff0f94" />

Here is everything new 

<img width="604" height="803" alt="image" src="https://github.com/user-attachments/assets/10344386-3423-4f02-ac0c-e56c3eb1a25c" />

And finally, here are the renders ! I spent about 10 minutes color matching things and adjusting lighting. 

<img width="900" height="1850" alt="Double Barrel Hotend" src="https://github.com/user-attachments/assets/11da3933-0e06-4a25-8940-128ac2d56bcf" />

<img width="1548" height="3811" alt="doublebarrelhotendnobg" src="https://github.com/user-attachments/assets/42c27ee4-65e3-4008-8139-e43ebdda7246" />
