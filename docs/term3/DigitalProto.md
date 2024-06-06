# **Digital Prototyping for Design**
## Module 4 & 5
> Sensing the body for meaningful interactions + Extended bodies with expressive Data

> Lina Bautista & Citlali Hernández

> 23-30 April 2024

## **Task: Prototype your wearable and experiment with your training model.**
_by Núria, Marius & Oliver_

This digital prototyping session centered on utilizing either our custom device or another form of movement tracking to generate artistic outputs. We explored how our daily movements could be translated into sound. Imagine if your music was influenced by your walking speed.

### Training the Model 

**From Movement to Data**

The initial step involved capturing data from the phone, such as room position, GPS, and speed, and sending it to Wekinator. Once in Wekinator, we trained our model to differentiate between walking (0) and running (1).

In a previous module, Citlali introduced us to a mobile app called “ZIG Sim,” which allows access to various phone sensors, including the accelerometer, gyroscope, microphone, and camera. This app can send sensor data via OSC messaging (among other methods) to another device for processing.

Using this, we had Mars run and walk around the room with the phone in his pocket. However, we quickly realized the room was too small to collect accurate data, so we moved the training to the roof for a larger, straighter space to gather more precise data. Although we wanted to investigate more types of movement, time constraints limited our focus to this aspect.

**Steps Taken**

The process from training to the final output was straightforward but required navigating through various software and interactions. Once the basics were understood, numerous opportunities emerged. The project's goal was to explore: "What if the songs you listened to changed based on whether you were running or not?"

Grabbing Data from Phone using ZIG Sim

1. Data Collection with ZIG Sim:
   - We used the ZIG Sim app on a phone to collect various data points, focusing on GPS, acceleration, and placement in the Z-axis.
   - The data was then sent to Wekinator.
   - To account for differences in individual movement, we trained the model on multiple people running and walking.

Training the Model in Wekinator

2. Model Training:
   - While collecting data from the phone, we simultaneously sent it to the Wekinator application on a laptop.
   - In Wekinator, we trained the model to recognize that running corresponds to a signal of 1 and walking corresponds to a signal of 0.

Sending Data to Max8

3. Connecting to Max8:
   - After completing the training in Wekinator, we connected the model to Max8.
   - The model was configured to send a signal of either 0 or 1 based on the movement data.

Converting Received Input to Sound in Max8

4. Sound Conversion in Max8:
   - Using the received signal, we created a simple flow of code in Max8.
   - This code switched between two sounds based on whether the signal was 0 or 1, effectively changing the music based on whether the user was walking or running.


### Result

In the end, we successfully created a model and code that enabled us to translate a person's running or walking into a corresponding song. It was exciting to see this in action because it suggests new ways for people to interact with their own movement, potentially enhancing experiences in dancing, running, or other sports.

<iframe width="560" height="315" src="https://www.youtube.com/embed/gc8T83aijoU?si=2YmEhxAFmuDO9I5V" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Click [**here to access the fabrication files.**](https://drive.google.com/drive/folders/1GyUP5U4Z0serdor8qmNFUkH-Sh0remx9)

#### Reflection: The four F’s of active reviewing

Facts:

- Working with Oliver, Carlotta and Marius was easygoing and pleasing.

- I discovered new apps and technologies like ZIG Sim, Wekinator or Max8

Feelings:

- I feel like having an unrelated delivery from our project at tjis stage was a bit distracting but also satisfying, for being able to disconnect from what we are doing and do a completely different task.

Findings:

- Sensors are not as complicated as I imagined and they have very fun and unexpected applications.

Future:

- I don't plan on researching more on this topic in the near future but I've enjoyed doing it now and I don't dicard it in the long run.
