Smart Control of Traffic Light System using Artificial Intelligence

This AI-driven traffic light control project uses real-time data to optimize signal timings, reducing congestion, delays, and fuel waste. By dynamically managing traffic flow and prioritizing emergencies, it improves travel efficiency and safety for both motorists and pedestrians.

<img width="307" alt="image" src="https://github.com/user-attachments/assets/c8b86752-908c-4e1e-ba2e-53274746db85" />


This Adaptive Traffic Signal Timer uses live images from the cameras at traffic junctions for traffic density calculation using YOLO object detection and sets the signal timers accordingly, thus reducing the traffic congestion on roads, providing faster transit to people, and reducing fuel consumption.

Inspiration

Traffic congestion is becoming one of the critical issues with the increasing population and automobiles in cities. Traffic jams not only cause extra delay and stress for the drivers but also increase fuel consumption and air pollution.

According to the TomTom Traffic Index, 3 of the top 10 countries facing the most traffic congestion are in India viz. Mumbai, Bengaluru, and New Delhi. People are compelled to spend hours stuck in traffic jams, wasting away their precious time commuting. Current traffic light controllers use a fixed timer and do not adapt according to the real-time traffic on the road.

In an attempt to reduce traffic congestion, we developed an improved traffic management system in the form of a Computer Vision-based traffic light controller that can autonomously adapt to the traffic situation at the traffic signal. The proposed system sets the green signal time adaptively according to the traffic density at the signal and ensures that the direction with more traffic is allotted a green signal for a longer duration of time as compared to the direction with lesser traffic.

Implementation Details

This project can be broken down into 3 modules:

Vehicle Detection Module - This module is responsible for detecting the number of vehicles in the image received as input from the camera. More specifically, it will provide as output the number of vehicles of each vehicle class such as car, bike, bus, truck, and rickshaw.

Signal Switching Algorithm - This algorithm updates the red, green, and yellow times of all signals. These timers are set bases on the count of vehicles of each class received from the vehicle detection module and several other factors such as the number of lanes, average speed of each class of vehicle, etc.

Simulation Module - A simulation is developed from scratch using Pygame library to simulate traffic signals and vehicles moving across a traffic intersection.

![vehicle-detection](https://github.com/user-attachments/assets/60832be9-36b6-4fc9-b338-0be8c9e8cf3a)


Signal Switching Algorithm and Simulation

![image](https://github.com/user-attachments/assets/fae8ebf1-6fda-4bc1-928b-72594ff5ad3b)



Prerequisites

Python 3.7

Microsoft Visual C++ build tools (For Windows only)

Installation

Step I: Clone the Repository

      $ git clone https://github.com/Rameshhosamani/SCOTLS-Project/edit/main/README.md
      
Step II: Download the weights file from here and place it in the Adaptive-Traffic-Signal-Timer/Code/YOLO/darkflow/bin directory

Step III: Install the required packages

      # On the terminal, move into SCOTLS/Code/YOLO/darkflow directory
      $ cd SCOTLS/Code/YOLO/darkflow
      $ pip install -r requirements.txt
      $ python setup.py build_ext --inplace
      
Step IV: Run the code

      # To run vehicle detection
      $ python vehicle_detection.py
      
      # To run simulation
      $ python simulation.py



