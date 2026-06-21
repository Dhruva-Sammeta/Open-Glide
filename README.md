# Open-Glide
This is the reference repo for the Opensource ardupiolt winged flight platform, Open-Glide, A 1.5m, redudent motors, multi part, 3d printed frame based UAV.
Open glide is meant to be a public reference, buildable platform where anyone with a printer and a few parts can make a robust airframe.
This project was no small feet overall, requiring tons of effort physically, what started out as this sketch:

# Quick Design history:
<img width="708" height="472" alt="image" src="https://github.com/user-attachments/assets/bf6c5130-65de-4f76-a644-69e82d8003ee" />


Where i basically just had to work with what components i had, which were definetley not limited in potential options or cheaper setups, but must be used in away where it's not specific or dependent on what i had:  
- Carbon fiber rod (12mm OD, ~1000 mm length)
- FS-i6S + 10ch Tx
- TBS Lucid H7
- 9g–90g servo motors x4
- 3S 2500 mAh LiPo battery
- Neo-6M GPS module
- A2212 BLDC motor x2
- D3542 BLDC motor x1
- 30-40A ESC x3
- ESP8266 NodeMCU
- 5V / 12V BEC
- 10 x 5 propellers x2
- LiPo (or Li-ion) battery
- 3D printer + Fliament
- Working tools (screwdrivers, glue, etc.)

With this, what i decided to do was split this project into parts:
## Main parts: Phase A: Proof of concept and flight validation, Phase A.5 extension of concept and integeration of true range components
Phase B: seaprate project, but spritual successor to Open Glide called *Ultra glide*.

TO achive this, the wing was a main priority, and was decided that a unibody wing would be best to use in sections rather then any sort of frame and skin design as printed wings have incredible torosional strength, going through my options for a 1.5m aircraft wing's aerofoil, the Naca 4412 came up as a good options for it's mix of camber, lack of thrust, and ease of design, and to further validate the strength of these potential sections, i ran cfd linked here:
<img width="1299" height="653" alt="image" src="https://github.com/user-attachments/assets/b3436faa-6042-436f-8024-26399f7ab14f" />
link to yt vid for ref: https://www.youtube.com/watch?v=w_1m_qjZ-Oc 

I used lattic internal suport to prevent tornsional being and any lateral loads are handled by the carbon fibre rod, giving us this:
<img width="1182" height="689" alt="image" src="https://github.com/user-attachments/assets/452c4268-c7bf-45ce-8193-dc30b2a136ca" />


And with such for the wing, i drafted the wing out asper the original design, while adding basic strut based fuselege bones to start out:
<img width="1054" height="772" alt="image" src="https://github.com/user-attachments/assets/e37994be-ce5b-4909-89f7-f0329a5a70c7" />

and moving further in CAD (fusion 360):
<img width="1389" height="823" alt="image" src="https://github.com/user-attachments/assets/7bf572f6-0646-4ca1-b348-f16432be6954" />
<img width="1100" height="711" alt="image" src="https://github.com/user-attachments/assets/5a3c4165-8be0-4cdc-a52d-f8bac7470fd0" />

## Note: I decided to switch to a tri-motor config mid CAD design as the weight was going to be too high, and deafeats the purpose of a flight test platform without that extra thrust, so:
<img width="1363" height="741" alt="image" src="https://github.com/user-attachments/assets/0ba2482a-f2de-4a6e-8999-e7f63a10f65d" />
# Overall cad:
<img width="1183" height="774" alt="image" src="https://github.com/user-attachments/assets/3247f970-bbfa-4b32-97d8-def2696b975a" />

## Trial & error: Struss design
the original version failed to have proper torsional supports for the fuselege, causing it to twist, seen irl as:
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/f718c295-8cb3-491d-bffe-3ae65a54c3cb" />
<img width="1600" height="720" alt="image" src="https://github.com/user-attachments/assets/c737528d-c475-4841-a8b5-457005c07141" />

and to address this, torosional strength was added:
<img width="1144" height="753" alt="image" src="https://github.com/user-attachments/assets/bd4bdb10-03e4-4e38-aa50-1454f9bbbd96" />

# Prototype 1:
<img width="1600" height="720" alt="image" src="https://github.com/user-attachments/assets/6a659197-c0ae-40c0-832f-349b8bd8d0c8" />
demo vid: https://youtu.be/HvyGQakFnIc (static due to lack of time to launch)

# Build Procedure:
To build Open Glide, you will first need to have a _3D printer, fliament, soldering iron, hex bits/allen keys, along with super glue is possible_, then aqquire the main parts list as seem in the BOM, mainly consisting of the Flight Controller, Receiver and transmitter, Servo motors, BLDC's, their compatable esc's, gps, node mcu and jumper wires.

1. Printing wing:

