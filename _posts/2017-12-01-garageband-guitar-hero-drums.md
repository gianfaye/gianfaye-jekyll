---
layout: post
title : "Garageband with Band Hero Drums"
tagline : 
category : blog
tags : [audio, recording, Garageband, Guitar Hero, Band Hero, drums, music, workaround]
---
{% include JB/setup %}

If you have a Band Hero drums from the Guitar Hero game franchise and want to know how to use it as a MIDI input to record a drum track on Garageband, there are hefty of resources already available online for you to set up:

#### External links:
* [YouTube: Band Hero PS3 Drums working with Garageband](https://www.youtube.com/watch?v=MnA5eKVlkJw)
* [Turn Guitar Hero Drums into an Electronic Drum Set](https://lifehacker.com/5419434/turn-guitar-hero-drums-into-an-electronic-drum-set)
* [Guitar Hero Drums as a real drum kit](http://vultrix.com/post/841779538/guitar-hero-drums-as-a-real-drum-kit)

If you've gone through these and you're already setup, good. However, I encountered an issue on Garageband where the drum track can be heard for a while and the sound would eventually disappear. I found out others also encountered this issue:

![Garageband Guitar Hero Drums Issue](/assets/themes/geekyll/images/garageband-band-guitar-hero-drums-issue.jpg)

I found a workaround for this.

My setup:
* Garageband 10.1.6 and the Band Hero drum kit for PS3
* The `MIDItar Hero v1.07.mxf` file from the last link above
* Max 7 - this opens the .mxf file
* MIDI Monitor
And this one is important if you encountered the same issue I pointed out above:
* MuseScore

I created an alarm device that will determine the temperature of your coffee (or tea), show you the status if it's still HOT, WARM, or COLD with LEDs (red, yellow, and blue respectively), trigger a warning alarm if it is getting cold and will buzz continuously when it eventually gets cold. 

## The Working Prototype
![Your Coffee is Getting Cold alarm device](http://i.imgur.com/zxCKLrG.jpg)

## Status: HOT

When your coffee is still hot, the red LED is on and the device will stay silent.

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:28.125% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BOmcDhDh5Wd/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">&#34;Your Coffee is Getting Cold&#34; ☕ alarm device pt. 1 - Status: HOT. When your coffee is still hot, the red LED is on and the device will stay silent. #DIY #maker #prototype #Arduino  #ArduinoUNO #sensor #alarm #coffee #tea</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">A video posted by Gian Faye (@gianfaye) on <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-12-29T12:12:03+00:00">Dec 29, 2016 at 4:12am PST</time></p></div></blockquote>
<script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

## Status: WARM

When you are neglecting your coffee for a while and it gets warm, the yellow LED is on and the device will trigger a warning alarm to get your attention. 

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:28.125% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BOmdiGvBlSj/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">&#34;Your Coffee is Getting Cold&#34; ☕ alarm device pt. 2 - Status: WARM. When you are neglecting your coffee for a while and it gets warm, the yellow LED is on and the device will trigger a warning (can I say warming? 😂) alarm to get your attention. #DIY #maker #prototype #Arduino #ArduinoUNO #sensor #alarm #coffee #tea</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">A video posted by Gian Faye (@gianfaye) on <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-12-29T12:24:58+00:00">Dec 29, 2016 at 4:24am PST</time></p></div></blockquote>
<script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

## Status: COLD

When you have failed to do the simple task of drinking your coffee while it's still hot, the blue LED turns on and you will hear a continuous buzz to again remind you of your failure and neglect. Time to brew another batch of hot coffee.

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:28.125% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BOmelwjBkmz/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">&#34;Your Coffee is Getting Cold&#34; ☕ alarm device pt. 3 - Status: COLD 😔 When you have failed to do the simple task of drinking your coffee while it&#39;s still hot, the blue LED turns on and you will hear a continuous buzz to again remind you of your failure and neglect. Time to brew another batch of hot coffee. ☕ #DIY #maker #prototype #Arduino #ArduinoUNO #sensor #alarm #coffee #tea</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">A video posted by Gian Faye (@gianfaye) on <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-12-29T12:34:12+00:00">Dec 29, 2016 at 4:34am PST</time></p></div></blockquote>
<script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

## The Parts

The device uses a temperature sensor [TMP36](http://www.analog.com/media/en/technical-documentation/data-sheets/TMP35_36_37.pdf) to determine your drink's temperature, a pressure plate for the device to determine if there is a cup of coffee present, a piezo buzzer for the sound alarm, and 3 LEDs to show you the status of your drink.

## The Pressure Plate

The device will only operate (check status and execute alarm) if you put your mug on it. I got the parts from [a kids science toy](https://www.instagram.com/p/1nvsARpcBG/?taken-by=gianfaye) and [a board game](https://boardgamegeek.com/boardgame/156091/sons-anarchy-men-mayhem). Partly a challenge to think about designing the plate with what I currently have at home, and make sure that it will be steady enough not to spill the drink all over my workbench. It's a makeshift switch that will close the circuit whenever some weight is added on the pressure plate. Works best for ceramic mugs.

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:28.125% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BOmfe2fBtk6/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">&#34;Your Coffee is Getting Cold&#34; ☕ alarm device pt. 4 - The pressure plate. The device will only operate (check status and execute alarm) if you put your mug on it. (Well, duh?) 😂 Got the parts from a kids science toy and a board game. #DIY #maker #prototype #Arduino #ArduinoUNO #sensor #alarm #coffee #tea</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">A video posted by Gian Faye (@gianfaye) on <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-12-29T12:42:00+00:00">Dec 29, 2016 at 4:42am PST</time></p></div></blockquote>
<script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

## The Buzzer

Also got this piezo from the kids science toy I used for the pressure plate. There's a limitation from Arduino where the volume cannot be configured, hence the need to cover it up because it's too loud.

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:28.125% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BOmhNuDBRos/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">&#34;Your Coffee is Getting Cold&#34; ☕ alarm device pt. 5 - The buzzer. Also got this piezo from the kids science toy I used for the pressure plate. There&#39;s a limitation from Arduino where the volume cannot be configured, hence the need to cover it up because it&#39;s too loud. 😡 #DIY #maker #prototype #Arduino #ArduinoUNO #sensor #alarm #coffee #tea</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">A video posted by Gian Faye (@gianfaye) on <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-12-29T12:57:08+00:00">Dec 29, 2016 at 4:57am PST</time></p></div></blockquote>
<script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

## The Sensor

Initially a challenge to ensure that the sensor touches the mug placed on the pressure plate. It needs to be flexible and not so wiggly so I braided the wires.

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-version="7" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:658px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);"><div style="padding:8px;"> <div style=" background:#F8F8F8; line-height:0; margin-top:40px; padding:28.125% 0; text-align:center; width:100%;"> <div style=" background:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACwAAAAsCAMAAAApWqozAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURczMzPf399fX1+bm5mzY9AMAAADiSURBVDjLvZXbEsMgCES5/P8/t9FuRVCRmU73JWlzosgSIIZURCjo/ad+EQJJB4Hv8BFt+IDpQoCx1wjOSBFhh2XssxEIYn3ulI/6MNReE07UIWJEv8UEOWDS88LY97kqyTliJKKtuYBbruAyVh5wOHiXmpi5we58Ek028czwyuQdLKPG1Bkb4NnM+VeAnfHqn1k4+GPT6uGQcvu2h2OVuIf/gWUFyy8OWEpdyZSa3aVCqpVoVvzZZ2VTnn2wU8qzVjDDetO90GSy9mVLqtgYSy231MxrY6I2gGqjrTY0L8fxCxfCBbhWrsYYAAAAAElFTkSuQmCC); display:block; height:44px; margin:0 auto -44px; position:relative; top:-22px; width:44px;"></div></div> <p style=" margin:8px 0 0 0; padding:0 4px;"> <a href="https://www.instagram.com/p/BOmjBjShzg6/" style=" color:#000; font-family:Arial,sans-serif; font-size:14px; font-style:normal; font-weight:normal; line-height:17px; text-decoration:none; word-wrap:break-word;" target="_blank">[Last video] &#34;Your Coffee is Getting Cold&#34; ☕ alarm device pt. 6 - The temperature sensor. This was initially a challenge to ensure that the sensor touches the mug placed on the pressure plate. It needs to be flexible and not so wiggly so I braided the wires. 😂 #DIY #maker #prototype #Arduino #ArduinoUNO #sensor #alarm #coffee #tea</a></p> <p style=" color:#c9c8cd; font-family:Arial,sans-serif; font-size:14px; line-height:17px; margin-bottom:0; margin-top:8px; overflow:hidden; padding:8px 0 7px; text-align:center; text-overflow:ellipsis; white-space:nowrap;">A video posted by Gian Faye (@gianfaye) on <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2016-12-29T13:12:57+00:00">Dec 29, 2016 at 5:12am PST</time></p></div></blockquote>
<script async defer src="//platform.instagram.com/en_US/embeds.js"></script>

## The Code

I initialized 3 constants for this sketch:

	const int sensorPin = A0; // connects the temperature sensor to an analog pin
	const int buzzerPin = 8; // connects the piezo buzzer to a digital pin
	const float baselineTemp = 25.0; // the base temperature to compare with what the sensor detects

On the setup:

	Serial.begin(9600); // opens a serial port
	// sets the LEDs (connected to pins 2, 3, 4) as output
	for(int pinNumber = 2; pinNumber < 5; pinNumber++){
	    pinMode(pinNumber, OUTPUT);
	    digitalWrite(pinNumber, LOW);  
	}
	pinMode(buzzerPin, OUTPUT); // sets the buzzer pin as an output

On the initial part loop:

	// determines the value of the sensor, this will be used to compute the voltage output
	int sensorVal = analogRead(sensorPin);

	// outputs the sensor value on the Serial Monitor for checking
	Serial.print("Sensor Value: ");
	Serial.print(sensorVal);

	float voltage = (sensorVal/1024.0) * 5.0; // converts the ADC reading to voltage

	// outputs the voltage reading on the Serial Monitor for checking
	Serial.print(", volts: "); 
	Serial.print(voltage);

	// converts the voltage to temperature in degrees Celcius
	float temperature = (voltage - 0.5) * 100; 

	// outputs the temperature on the Serial Monitor for checking
	Serial.print(" , degrees C: ");
	Serial.print(temperature);
  
	// will be used to print the status on the Serial Monitor
	String tempStatus = ""; 

Determining the temperature:

	// determines if drink is COLD
	if(temperature < baselineTemp) {
	    // if temp is less than 25 C, turn the blue LED on
	    digitalWrite(2, HIGH); // blue
	    digitalWrite(3, LOW);  // yellow
	    digitalWrite(4, LOW);  // red
	    
	    tempStatus = "COLD :("; // sets the status to print on later

	    // turns the buzzer on
	    digitalWrite(buzzerPin, HIGH); 
	    tone(buzzerPin, 1024, 3000); // (pin, frequency, duration) 
	    // the duration is the same as the delay time for the loop to mimic continuous buzzing sound
	}
	// determines if drink is WARM and getting cold
	else if(temperature >= baselineTemp && temperature < baselineTemp + 3){
	    // if temp is 25 C to 27 C, turn the yellow LED on
	    digitalWrite(2, LOW);  // blue
	    digitalWrite(3, HIGH); // yellow
	    digitalWrite(4, LOW);  // red
	    
	    tempStatus = "Still WARM but GETTING COLD!"; // sets the status to print on later

	    // turns the buzzer on
	    digitalWrite(buzzerPin, HIGH);
	    tone(buzzerPin, 1024, 1000); // (pin, frequency, duration) 
	    // the duration is less than the delay time to mimic a warning alarm sound
	}
	// determines if drink is still HOT
	else if(temperature >= baselineTemp + 3 && temperature < baselineTemp + 8){
	    // if temp is greater than 27 C but less than 35 C, turn the red LED on
	    // I need to set a cap at 35 C because the temp reads very high when there's no subject to test on
	    digitalWrite(2, LOW);  // blue
	    digitalWrite(3, LOW);  // yellow
	    digitalWrite(4, HIGH); // red
	    
	    tempStatus = "Still HOT :)"; // sets the status to print on later
	}
	// if there is no mug present on the pressure plate, do nothing
	else{
	    digitalWrite(2, LOW); // blue
	    digitalWrite(3, LOW); // yellow
	    digitalWrite(4, LOW); // red

	    tempStatus = "Missing subject"; // sets the status to print on later
	}

	// prints the status of the temperature
	Serial.println(" , Status: " + tempStatus);

	// three-second gap for each check
	delay(3000);

## Breadboard View

![Your Coffee is Getting Cold alarm device breadboard](http://i.imgur.com/qSgIDEw.png)

## Schematics

![Your Coffee is Getting Cold alarm device schematics](http://i.imgur.com/FBR4ISP.png)

Total time spent for this project: `3 hours` (including the time spent figuring out the design with the available resources)

That's it! Let me know on the comments section below if you see points of improvement on this project or if you created your own. :) Enjoy your cup of hot coffee.

#### Related post:
* [Arduino: Getting Started](/blog/arduino-getting-started/)

<hr>
