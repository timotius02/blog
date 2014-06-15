---
layout: post
title: Computer Graphics and Socket.io
---


I have a deep fascination with anything real-time. Whether it was a simple messaging app, or even a full blown real time strategy game, I've always been curious to try my hand on something realtime. So when I was introduced to [Socket.io](http://socket.io), I couldn't be any happier.

##The Project [http://graphics3d.herokuapp.com/](http://graphics3d.herokuapp.com/)

To run a quick demo of the project, travel to the website and press the example button and the convert button. A cube and a sphere will appear on the canvas. The cool part is if you use you smartphone (Try using Chrome Mobile for this) and travel to the link, you can check the box labeled "Is controller?". As soon as you do, the phone will start acting as a remote control and the canvas image will begin to rotate according to the orientation of the phone. Pretty cool huh?

##Socket.io

The premise of Socket.io is "simple, real-time bidirectional event-based communication". What this means is that it takes the newly standard websocket technology and make it easier to implement within webapps. I wanted to use Socket.io for my Computer Graphics final project so I decided to combine the simple three dimensional graphics that I learned in class with the cross communication realtime of Socketio. 

##The Culling
In terms of the graphics side of things, there was nothing too complicated. In order to make it as simple as possible, I only good-old HTML5 canvas along with many of its native drawing functions. The most important part is the [Back-Face Culling](http://http://en.wikipedia.org/wiki/Back-face_culling) technique to produce the seemingly three dimensional image, which is done through the use of triangles representing the faces of the three dimensional figures and applying the back-face culling formula as well as some vector algebra to discern which faces were visible on screen. 

##Socket.on('rotate', ...)
Using socket.io, I can allow for simple, real-time communication between a smartphone and the client using the server as the middle-man. I'm not going to go over in full detail how to use Socket.io, but you should travel to their website [Socket.io](http://socket.io) to learn about that amazing module. Basically, combined with the deviceOrientation event, I was able to use the browser on my phone to send my phones orientation to the server, which is then sent to the client and applied to image image on screen. It's very neat.

##Final Words
SInce the graphics engine was made to be similar to the one that I had designed for Computer Graphics in C, it has many capabilities other than the real time connection. Using the right command functions, you can create many 3D animations using the text area and you can import both command and import files directly two the webapp without the need of using any server functionality. 

The command file requirements can be found [here](http://69.55.54.194/pbrooks/spring2014/materials/graphics/Object3d-Interpretation.pdf). 

<p class='message'>Note: Since I was running out of time, there are currently no implemented lighting commands or surface color command within the app.</p>
