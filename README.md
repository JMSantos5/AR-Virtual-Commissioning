---CONTEXT---

Project for my master's dissertation titled "Augmented Reality for Virtual Commissioning within Modular Production Systems".

---OBJECTIVE---

Exploring how viable it is to utilize Augmented Reality (the presentation of virtual objects in a real environment, through a screen, for example) 
as a way to perform Virtual Commissioning (testing the controller code of a real system by virtually simulating said system) 
for the addition of modules to Modular Production Systems (systems composed of multiple modules that execute independent tasks, but operate together as a complete system).

This concept would allow someone to test the controller code of a module and see it operating in an existing Modular Production System before committing to buying said module.

---PROTOTYPE---

In the context of the dissertation, I developed a prototype by using a small-scale Modular Production System composed of 2 Fischertechnik’s 24 V Conveyor Belts (https://www.fischertechnik.biz/conveyor-belt-24-1).
The solution allowed me to simulate the addition of a new conveyor to this system, and can be divided into 3 main parts.

Unity:

I made a Digital Twin of the conveyors by constructing a 3D model of them using Blender, and then importing it into Unity.

Using Unity, I developed a C# Augmented Reality application that allowed me to see the Virtual Conveyor wherever I put a QR code, operating as if it were a real conveyor.

Java:

I developed the Modular Production System's controller code using JADE (Java Application DEvelopment Framework), 
a framework that allowed me to create a Java application to program the logic of the system using a Multi-Agent System approach. 

I then used a WebSocket protocol to allow communication between the Java and the Unity applications, 
which allowed me to Virtually Commission the real conveyor (test its control code by simulating it) and see how it would operate in the real world through my phone's screen.

Node-RED and integration:

The final step was testing the virtual module's code by making it part of the real Modular Production System. 
I programmed the real conveyors with Node-RED using a Revolution Pi, a compact control system powered by a Raspberry Pi microprocessor, 
to allow them to communicate with my Java controller application via a WebSocket protocol. 

Afterwards, I simply had to place the QR code in the position where I would want a new conveyor to be added, and I could see how the final system would operate.

Video link to check the prototype in operation: https://drive.google.com/file/d/1D1VCTSG_krM1Nx2iWjZdPSCOtW3ntOr8/view?usp=drive_link

---SPECIAL THANKS---

I publish this project without leaving a special thanks to my dissertation Advisor, Professor and Researcher André Dionísio Bettencourt da Silva Parreira Rocha,
and to the institution where I developed it, the NOVA School of Science and Technology from Universidade NOVA de Lisboa!










