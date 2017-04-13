---
layout: page-left-menu
title: Getting started with the Z-ranger deck
permalink: /getting-started-with-z-ranger-deck/
page_id: getting-started-z-ranger-deck
---

{% si_intro The Z-ranger deck %}
The Z-ranger deck contains a VL53L0x Time-of-Flight (ToF) laser-ranging sensor and has a 1-wire memory which enables the Crazyflie to automatically detect the Z-ranger deck.
The sensor can measure the distance up to 2 meters from the Crazyflie to the ground. The deck can be only be installed on the bottom of the Crazyflie. For more information about how to mount an expansion deck please see the [Getting started with expansion decks](/getting-started-with-expansion-decks/) tutorial.

To be able to use the Z-ranger deck you need to update the Crazyflie to the latest firmware. For more information on how to update the firmware, see the [download latest firmware](/getting-started-with-the-crazyflie-2-0/#latest-fw) section in our getting started with Crazyflie 2.0 tutorial.

{% endsi_intro %}

{% si_step  Using the height-hold mode %}

To use the Z-Ranger deck you need to use the Python client and set up a connection with your Crazyflie.
For more information about how to set up your Crazyflie and install the client go to [Getting started with the Crazyflie 2.0](/getting-started-with-the-crazyflie-2-0/).

In the client, go to Assist mode and choose Height-hold mode in the dropdown menu.
{% img Z-ranger deck tutorial; wide; /images/tutorials/height-hold.png %}

Place the Crazyflie 2.0 on the floor in an area with extra room for flying, then
press the assisted mode button on the gamepad to activate the height-hold mode.
The Crazyflie will now take off and hover at a height of 40 cm.

To control the Crazyflie use roll/pitch as normal and use the thrust to change
the height-hold set-point. Releasing the height-hold button will de-activate
the mode and the thrust input will work as normal (i.e you will have to give
thrust for the Crazyflie not to drop).

{% endsi_step %}

{% si_step  User-interface guide %}

Below is a short explanation of the user-interface.

{% img Z-ranger deck tutorial; wide; /images/tutorials/client.png %}

1. Target set-point height (in meters)
2. Height error (in meters). I.e difference between the set-point and measured height.
3. Target set-point height (in meters)
4. Measured height (in meters)

{% endsi_step %}

{% si_step  Measurement details %}

When the sensor measures the distance to the ground it will not use a single point.
Instead the detection will use cone (see below) where the sensor will report the
closest detection. This means that the higher the Crazyflie is the larger the
area of detection. For instance this could be an issue if the Crazyflie gets
close to a wall, then it will report the distance to the wall instead of the
floor.

{% img Z-ranger deck tutorial; wide; /images/tutorials/sensor.png %}

{% endsi_step %}