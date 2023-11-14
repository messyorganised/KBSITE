# NBN FTTN Research

## Intro

I have recently relocated from a Fixed Wireless connection to a FTTN. Thinking that I could finally get that 100/40 for my projects. Boy was I wrong.

Immediately after I have gotten everything set up I realised that I am currently only getting 10% down / 5% up of what has been advertised by all ISP

It is definitely a big slap on the face. But I pushed through and read through articles after articles, trying to figure out how to resolve my horrible speed issue.

In the end I manage to convince my ISP to send an NBN technician over to investigate the problem. Which they are yet to attend.

In saying that, I learned a few things that might help other people who are in my position.



### What happened?

I learnt that in March 2022, NBN has implemented 2 new VDSL2 functions on their network; Save Our Showtime (SOS) and Robust Overhead Channel (ROC). Below are a summary of what they are:

#### **Save Our Showtime (SOS)**

Think about watching a movie online and suddenly the video starts buffering or the quality drops. This is because your internet traffic is congested. Save Our Showtime, or SOS, is essentially a mechanism that NBN has, where it prioritizes certain types of data over others to ensure a smooth experience. In this case, it prioritizes video streaming or video conferencing traffic to prevent any disruptions during 'showtime'. Its like giving a VIP lane to movie streaming data on a busy internet highway.

#### **Robust Overhead Channel (ROC)**

The ROC compliments the SOS service. This is a bit like a special communication line or pathway used by the NBN network. It's designed specifically for control and management information. Think of it like the manager in a big factory; it doesn't directly produce goods but it keeps the whole operation running smoothly. If the normal data channels are like cargo trains carrying heavy data packets, the ROC is like the control tower, ensuring everything is moving as it should.



### Why did they do that?

Now, don't ask me why the do it. From what I can see, this update was supposedly meant to improve their VDSL connection for all FTTN / FTTB service. However, in doing so they have caused some old hardware to be incompatible.&#x20;

Hardware that doesn't support the service will either stop working completely or would experience extreme amount of frequent packet loss throughout the day. I was a victim of the latter.



### Does that mean I'm going to have to chuck my old gear?

After further investigation, I discovered that there is a third Acronym that stand under the spotlight for this whole debacle; Seamless Rate Adaptation (SRA).&#x20;



**Seamless Rate Adaptation (SRA)**

Let's imagine the internet service as a delivery truck running on a highway. Sometimes the road is clear and the truck can speed up, but other times, due to traffic or bad weather conditions, the truck needs to slow down.

SRA works very much the same way in the internet world. It is a feature employed on NBN networks that allows your internet connection speed to automatically adjust to the best possible speed it can provide depending on the current network conditions. This happens 'seamlessly', meaning you as a user won't notice these adjustments – the aim is to ensure a smooth, uninterrupted browsing experience regardless of what's going on 'on the road'.

In other words, _i**t ensures that your internet speed is always optimally set to provide a stable connection, by adapting to any changes in the network conditions as they happen**._ This is particularly useful in situations where the quality of the line or signal might fluctuate.



#### What does it do?

Now I'm no expert in NBN technology, but reading from the article that Draytek (hardware that I use) has published. It appears to be the minimum requirement for you to have an uninterrupted connections.

> _For CPEs not supporting these new functions, another function, Seamless Rate Adaptation (SRA) will be required to ensure connectivity under certain noisy conditions._

The article can be access via the link below.

{% embed url="https://faq.draytek.com.au/2022/06/06/nbn-vdsl2-connection-update/" %}

Lucky enough, my ancient hardware is the first thing on the list. Although it is not something to be brag about, this means that my hardware is compatible with the bare minimum requirement. Although there are few extra steps that I needed to take to make it happen. Such as firmware upgrade and utilising the correct latest firmware. I have finally made my modem a FTTN compatible device.&#x20;



### But...

Unfortunately this does not resolve the underlying issue that I have been having since getting this FTTN connection; which is the 10% /5% performance in comparison to what was advertised. Hence why the NBN tech is being sent to my site for further investigations.



I hope that some of you find this article helpful and some resolved their internet issues on FTTN connection with this article. Hope you have a good day.
