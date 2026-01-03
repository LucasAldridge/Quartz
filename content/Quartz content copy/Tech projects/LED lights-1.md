I want sexy lights. 

Currently, sexy lights are expensive, you must buy them from Govee, or Nanoleaf, or Phillips. However, like all things, it is much, MUCH cheaper to do it yourself (mind you, moderately to severely more work)

And so I have decided to embark upon my quest for cheap, sexy LED lights. For this I need three inrgedients

## 1. ESP-32

An ESP-32 is a cheap ($5) microcontroller with built-in bluetooth and wifi capabilities. The kind I have is powered via a USB-C cable, and with the soon to be mentioned breadboard jumper cables, it can be connected to your soon to be mentioned LED lights

## 2. Lights

You should probably get some lights for your lighting project. Strip lights are what I'm looking at for my purposes. Peep Aliexpress and look for a nice, dense LED strip with individually addressable bulbs. The names are confusing but what really matters, is the length (just buy like 5m to be safe), density (>=60), and whether they are individually addressable. If your lighting application needs to get wet, that's when you need to worry about IP ratings. IP comes in 3 values (30, 60, and 67.) The higher the number, the more wet it can get (and you know we keep it wet)

## 3. Breadboard jumper cables

These are what you use to connect your lights to your ESP32. Get the Male->Female ones... a lot are just Male->Male, which in this case it no good. Peep Aliexpress if you want em cheap. 

I myself have successfully acquired all of these, so now it's a matter of hooking the ESP to my computer, going to install.wled.me, and downloading WLED onto the ESP. From there, you can configure the wifi settings by connecting to the WLED-AP network (via your phone) that your ESP automatically starts emitting once WLED is installed. Hit settings, connect it to your actual Wifi network, download the WLED app (again, on your phone), then either manually input the Client ID found in the WLED-AP wifi settings for your lights, or (in some lucky cases) just hit the "discover devices" button on the app.

## 4. Control box
I need to make a control box. I'm thinking 3D printed Black. It needs
- Switch on and off
- knob color
- knob brightness
- 