# **Measuring the World**

> Oscar Gonzalez, Adau Surinach & Guillem Camprodon

> 7-9 February 2024

---
[Sense-Making Journal: Healthier City Navigation](https://hackmd.io/uqV0O0QqQgC3rkSMgWcbgg?both)
====================


***MDEF:** Measuring the world / A world in data activity report.*

***`Team name`** Núria, Jorge D., Oliver, Marius, Carlotta and Everardo*

**Journal Index**

[TOC]

## `Objectives` -> `Hypothesis`

### Brainstorming
![Post-it ideation](https://hackmd.io/_uploads/SyVFyeWoT.jpg)

### Project Goals
**Objective:** ~~We want to navigate the city in the healthiest way possible~~ We want to have an unobstructed view of the sky in Barcelona. 

**Questions:** 

**Sound pollution and air pollution**

- Are the sound levels throughout the city below the healthy limit? (85 dB) Day? Night?

- Is the air quality at a level that is healthy to exercise outside?

**Sunlight and visible sky**

- Can we decide where to go have a vermut depending on the sun?

- **_Can you walk around the streets of Bcn and get a healthy amount of sunlight?_**

- **_Is the sky in Barcelona visible enough to not feel caged?_**

**Illumination and street safety**

- Are the streets of the city illuminated enough to feel safe for walkers? (Specially women)

**Sensorly and mobility inclusion**

- Is the Barcelona metro sensorly inclusive?

- Is every part of the city reachable for everyone? (mobility & inclusion)

- Are the lightlevels in the metro at a level that is positive for ones mental health? 


### Hypothesis

There is not enough connection to the natural sky in Barcelona.

### Tips
- Try and focus on one area instead of all the things at once
- Focus on things you are passionate about as it will be easier to research and spend time on


## `Hypothesis` -> `Data`

### Tools selection

We fighted for the Raspberry Pi Camera for our exercise. We plan to gather data about the direct sunlight that the streets of Barcelona get, to find a way to navigate through the city in a healthier way, wether is gettinf vitamin D from the sun during the winter, or avoiding the sun rays during the summer.

We consider a camera is very important for our exercise because we don't want to measure the temperature or the light level, but we want to see what areas of the sidewalks are in contact with sunlight.

We though about alternatives, when we were discussing with other groups, and found some ways to change our exercise, through a physical action for example, but we still think the camera is the one that fits us the most.

![RaspberryPiCamera](https://hackmd.io/_uploads/ByFqkrzip.jpg)


### Tool usage documentation
_How can others replicate your data capturing process again?_

Our data capturing process is easyly replicable. They would need to gather the materials, preferably 1 Raspberry Pi camera and 5 smartphones, and divide the group on the following areas of Barcelona to do the exercise: Sagrada Familia, Eixample Esquerra, Putxet, Ciutat Vella, Sant Martí and El Clot/Poblenou.


#### Data capturing strategy

We decided to take advantage of the little time we had to collect as much data as possible, but we only had a Raspberry Pi camera. To make the best use of the exercise, we decided to use the cameras of our phones, so we could capture more images simultaneously.

Each of us had to complete the following actions:

- Take 10 pictures of 10 different streets in our neighborhood during the day.
- Take 10 pictures of 10 different streets in our neighborhood during the night.

In this way, being 6 in the group, we managed to collect 120 images with relevant information for our exercise. 


#### Materials needed

- Raspberry Pi Camera (only one person used it)
- 5 smartphone cameras (the rest of the group)

#### Detail setup instructions (Raspberry Pi Camera)


1. Insert an micro sd card into your computer and load Raspberry OS on it
2. Connect the Raspberry Pi to a power source (powerbank, wall outlet through a 5V charger)
3. Connect the Raspberry Pi to a monitor and a keyboard (*this will make it easier to do the next few steps*)
4. When the Pi has booted up completely,you will be prompted to login with the username and password you set up during step 1. You can begin the process of connecting it to a wireless network.

(*If using a mobile hotspot as the wireless network and you are using an iPhone, make sure that the "maximise compatibility" feature is turned on in your hotspot settings. If you are using an android device it should be fine.This is because older models of the raspberry pi cannot connect to a 5G network natively.*)

5. In the terminal interface of the Pi run the command "sudo raspi-config", this will bring up the raspberry pi configuration window. Navigate to and select the wireless configuration option. 
6. Connect to a Wireless Network ~ You will be prompted to enter the name of your wireless network, hit "Enter" then enter your network's password nad hit "Enter". You should now be connected to the WiFi network.
7. From the terminal inside the Raspberry Pi OS you need to install the RPi-Cam-Web-Interface. You can follow the instructions to do so [here](https://elinux.org/RPi-Cam-Web-Interface)

*Once you've installed this interface, you can  move on to the next steps*

8. To check that your pi has connected to your desired network, install a network scanning software like [Advanced ip scanner](https://www.advanced-ip-scanner.com/es/)
9. Run this program, and start scanning your network for IP addresses connected to the network. 
10. You will be able to identify your raspberry pi's IP address by its device manufacturer identification in this case "Raspberry Foundation"
11. Once you've found your raspberry pi in the list of connected devices, copy and past the pi's unique IP address into your web browser of choice with /html at the end. **e.g.** 192.0.2.1/html
12. Once connected to the Pi via browser you should see the RPi interface dashboard with a live feed from the camera, and a series of buttons for various actions through the camera like taking photos, recording video or timelapse and accessing the stored photos and videos you've taken. 
![RPi Cam Control v6.6.26 mycam@pi.jpeg](https://hackmd.io/_uploads/Hk5J5DMsT.png)

13. Congratulations! You are now set up and ready to take pictures with your raspberry pi and camera. :D



#### Data collected

Daytime photos
![IMG-20240208-WA0017 (1)](https://hackmd.io/_uploads/H1r5CEziT.jpg)

Nightime photos
![IMG_4756 (1)](https://hackmd.io/_uploads/rJ5YCVfi6.jpg)


### Tips

- Try and focus on the same time frame for each pictures to get a better result
- Take more time to specify on different areas at different timeframes to get wider range of data
- Explore a wider range of areas to get a completer set of data



## `Data` -> `Information`

### Data summary

#### Brightness levels depending on the neighbourhood

To analyze the data we used a variety of methods. The first one we did was using a python code to create grayscale images and then score the brightness between 0 (darkness) and 255(ultimate brightness). 
[Images Taken](https://drive.google.com/drive/folders/1qAixeyf44rdwjEV9SunS5fq08_O7n1Ge?usp=sharing)
[Code Used](https://drive.google.com/file/d/1QKK2Q41YYNZMabSOUOeHcx8p3JIgEbuU/view?usp=sharing) 
[Data Used](https://docs.google.com/spreadsheets/d/1l1ePnkekDLylqL7D_hXzZKzL3lYDbhDb4eF5P5soyEM/edit?usp=sharing)

It is important to say that as the eixample images were shot with the raspberry pi the quality and light could potentially be different then the images shot with the phone and cameras. These images were then exported into a csv file and used to create the following graphs.

*Average brightness in each neighbourhood at day and night*
![chart](https://hackmd.io/_uploads/BJWYvDGsp.png)

*Brightness per situation per neighbourhood*

The next graphs created were scatterplots of each neighbourhood using the data collected during day and night 
to see the relative brightness of each picture at different times of day. 

![Lighting Situation Gotica_Raval](https://hackmd.io/_uploads/SJ23vDfiT.png)
![Lighting Situation Eixample](https://hackmd.io/_uploads/rJ2hDDGoT.png)
![Lighting Situation Sant Marti](https://hackmd.io/_uploads/Syn2vwMsT.png)
![Lighting Situation Sagrada Familia Night](https://hackmd.io/_uploads/ByhhDDfj6.png)
![Lighting Situation Putxet Overday](https://hackmd.io/_uploads/S132Dwfja.png)
![Lighting Situation Sant Marti Night](https://hackmd.io/_uploads/H133wDGop.png)
![Lighting Situation Poblenou Morning (1)](https://hackmd.io/_uploads/S1T-dwfiT.png)


#### Lighting Maps Using Found Data vs Collected Data

Using the data we collected about the light at night and the average levels in each neighbourhood we mapped the level of light pollution that could be found. (With this map the whiter the yellow the color the more light pollution)

![dtafromus-2](https://hackmd.io/_uploads/H1OlmK7iT.jpg)

We then went and looked for more opensource data that we could use to create a better map that takes more factors into account then just the small sample we had. The data we used was [LightPollutionMap](https://www.lightpollutionmap.info/#zoom=12.21&lat=41.3796&lon=2.1524&state=eyJiYXNlbWFwIjoiTGF5ZXJCaW5nUm9hZCIsIm92ZXJsYXkiOiJ2aWlyc18yMDIzIiwib3ZlcmxheWNvbG9yIjp0cnVlLCJvdmVybGF5b3BhY2l0eSI6NjAsImZlYXR1cmVzb3BhY2l0eSI6ODV9)
![datafromothers-2](https://hackmd.io/_uploads/r1Lgmtmia.jpg)
#### Comparison between real data recolected by us, and SketchUp shadow plug in


![Comparison2](https://hackmd.io/_uploads/BJRW1wfsT.jpg)

![Comparison2-02](https://hackmd.io/_uploads/rkcS1DMop.jpg)

![Comparison2-03](https://hackmd.io/_uploads/HklI1Dzsp.jpg)

![Comparison2-04](https://hackmd.io/_uploads/Sk48kPziT.jpg)

![Comparison2-05](https://hackmd.io/_uploads/rku81DGsT.jpg)


<br></br>

## Learning Outcomes

### Conclusion of the Results

With the data we have recollected and the information already existing in the shadow SketchUp plug in (having previously compared and verified that they are true), we have designed a reccomended route for people living in Ciutat Vella, Eixample and Sagrada Familia to have a healthy 20 minute walk in the sun that will:

   - **Vitamin D synthesis:** Sunlight is a natural source of vitamin D, and exposure to sunlight triggers the synthesis of this essential vitamin in the skin. Vitamin D is crucial for bone health, immune function, and overall well-being.

   - **Mood improvement:** Sunlight exposure stimulates the production of serotonin, a neurotransmitter that contributes to feelings of well-being and happiness. Sunlight exposure is associated with improved mood and can help alleviate symptoms of conditions like seasonal affective disorder (SAD).

   - **Increased energy levels:** Sunlight exposure can boost energy levels and reduce feelings of fatigue. The combination of fresh air and natural light during a walk can invigorate and rejuvenate the body.

   - **Better sleep:** Exposure to natural light during the day helps regulate the body's circadian rhythm, promoting better sleep quality. This can positively impact overall health and well-being.

   - **Physical activity:** A 20-minute walk provides a moderate form of exercise that contributes to cardiovascular health, improved circulation, and weight management. Regular physical activity is associated with numerous health benefits, including reduced risk of chronic diseases.

   - **Stress reduction:** Spending time outdoors, especially in natural settings, has been linked to stress reduction. The combination of sunlight, fresh air, and nature can have a calming effect on the mind and body.

   - **Improved concentration and focus:** Physical activity and exposure to sunlight have been shown to enhance cognitive function. Taking a short walk in the sun may help improve concentration and mental clarity.

   - **Enhanced immune function:** Adequate vitamin D levels, obtained through sunlight exposure, play a role in supporting a healthy immune system. A well-functioning immune system is crucial for defending the body against infections and illnesses.


<iframe src="https://drive.google.com/file/d/1ABF3Y_fuJx2FqJjUHfWB7HlzsLbcS-vG/preview" width="640" height="480" allow="autoplay"></iframe>



### Tips

One thing we could improve in the future is using the same tool for all the images. The initial plan was to use the Pi to take most of the pictures in the neighbourhood and suplement those with photos from phones when needed. 

The setup took much longer than we expected, so we chose to mostly rely on our phone cameras which led to images that varied in quality more then if one single camera had been used with the same settings. 

We learned that collecting data means needing to adjust to different set backs and reflecting on which ways your data might differ then the plan.  

<br></br>



## Future explorations

Build an interface similar to Google Maps, that could reccomend healthier routes for people navigating the city depending on:

- Direct sunlight contact (the one we explored)
- Visiblility of the sky
- Sound pollution levels
- Air pollution levels
- Street illumination and street safety
- Sensorly inclusivity

Taking data from already built networks in the city like Smart Citizen or other similar projects.

_As an inspiration, we have found a similar project that modeled direct sunlight and shades and developed a tool that creates optimal routes for heat prevention: seeking shady sidewalks, drinking fountains or places to take shelter._

https://cool.bcnregional.com/ 

![Inspiration](https://hackmd.io/_uploads/BkQO5_Gi6.png)


## Presentation

<iframe src="https://drive.google.com/file/d/1oZE9mHjNlKVq8SvNcj0Hfhg5m0Z-4nVO/preview" width="640" height="480" allow="autoplay"></iframe>

<br></br>

# Final reflection