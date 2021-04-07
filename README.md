# Box_of_Help_CUNY_Hackathon_2021

Check out the devpost submission here: https://devpost.com/software/box-of-help

Video demo: https://www.youtube.com/watch?v=5SW8xD-G8Uk

**Inspiration**

The other day my mom went to my grandparents’ room to call my grandma for lunch only to see her on the floor and barely conscious. My grandmother had been trying to get a glass of water on the other side of the room without her walker, causing her to stumble and fall. When we asked her why she decided to get herself water instead of calling for help, she said, “I tried to, but no one heard me”. After that incident I was determined to do something so that a similar incident, that could yield a more devastating outcome, would never happen again.

**What is it and how does it work?**

The “Box of Help” is a voice activated device that sends a notification to all mobile devices in the household stating that “The caller needs assistance”. For the hardware, I used a Raspberry Pi 3B+ for the “brain”, and connected it to a microphone for voice control and an LED to serve as a visual indication that your request has been heard. For the software I first worked on the implementation of voice commands through Google’s API. Through the API, I was able to take a voice command and turn it into a text format, allowing me to check if the correct command to “call for help” was called. If the voice command is successfully verified, the program would send a notification to all connected mobile devices through IFTTT, a free, web-based service that allows users to create chains of conditional statements triggered by changes that occur within other web services. The notification would be sent through the IFTTT app, which is available on iOS and Android devices. When the notifications have been sent, the LED will blink, giving a visual indication that the call for assistance has been sent.

**Challenges**

The one thing that took up most of my time was figuring out how to implement Google’s speech-to-text API. Working out what credentials were and downloading and using JSON files became really confusing and I kept losing track of which files were for what purpose. Thankfully, there are many forums and websites that can help you get started.

Another challenge was figuring out how to send a notification to everyone's mobile devices (phones, tablets, etc). Originally, I was going to use a free service called Pushbullet, which effectively would have yielded the same results I got with IFTTT, but the only caveat (and this was a deal breaker) is that the pushbullet app is not available for iOS devices, which was unfortunate because I only realized this AFTER I set everything up using Pushbullet, so I had to scrap what I had and set out to find a new solution.

The biggest challenge of all though ended up being something totally unpredictable. My area experienced a power outage. I managed to film a video of my device working literally minutes before the power went out. I’m actually typing this devpost submission on my phone (which is not very fun). At this point I can’t really finish everything I wanted to achieve with my project (because I can’t test it out without an internet connection) but I managed to achieve my main goals for this project, so I’m grateful for that.

**Takeaways**

Learning how to use an API and embed it with my code was a daunting task, but I’m so glad I did it. Especially since I used python, which is a language I haven’t used since my sophomore year of high school, I learned (and relearned) a lot of syntax, and my confidence in coding with the language has dramatically increased.

But the biggest takeaway was how much fun I had while messing around with the hardware. It felt like I was playing with LEGOS again, but the pieces were much cooler this time around. Seeing a visual result of something I’ve worked on for hours gave me a feeling of satisfaction I’ve never felt before. This project definitely made me want to work on more hardware-based projects in the future.

**Where will the Box of Help go next?**
I know for a fact that I can significantly downside the size of this device. It’s not huge (a little bigger than a google home mini), but upon doing some research, there are some Wifi based microcontrollers (such as the ESP8266MOD) that are significantly smaller and can do the same tasks. Another thing that could be improved on is the notification system. If you were at school, work, or outside of the house in general, it would be pointless to receive a notification. So to combat this, a GPS system could be implemented, where the position of the “Box of Help” would be constantly tracked, and when a call for help would be called, it would send a notification only if the members of that household were within a 100ft radius of the device. There could also be a setting to toggle notifications on despite being out of the "get a notification" radius for people who want to get notifications no matter where they are.

This device doesn’t only have to be restricted to the elderly calling for help. Another use case I could see my family using this would be when the person cooking has to tell everyone that the food is ready. Instead, the person cooking could just tell the device to call everyone to the dining room to eat, and creating more than one voice command is simple, since all of the framework is in place. The device could also be used as a smart home device, and could control smart home devices such as lights and blinds. The sky’s the limit, and this hackathon made me fully realize that.
