
Engine System Documentation

Overview

The EngineSystem generates power for the car by combining the Motor, Pistons, and Crankshaft. Each part plays a specific role in creating and managing this power, which is then used to drive the car.

Components and Roles

Motor  
- Role: The motor is the primary power source for the engine. It generates rotational energy used to drive the pistons and crankshaft.  
- Fields:  
  - `horsepower`: Defines the motor’s power output, impacting the overall strength of the engine  
  - `fuelType`: Specifies the type of fuel (e.g., Diesel or Gasoline), affecting the motor’s performance and efficiency

Piston  
- Role: Pistons convert the energy generated by the motor into linear motion. This motion is essential for creating the rotational force needed to drive the crankshaft.  
- Fields:  
  - `diameter`: Represents the piston’s size, which influences power output  
  - `strokeLength`: Defines how far the piston moves, affecting efficiency and power  
  - `material`: Indicates the piston’s material, which impacts durability and performance

Crankshaft  
- Role: The crankshaft converts the pistons' linear motion into rotational motion. This rotation is essential for transferring power from the engine to the transmission.  
- Fields:  
  - `numberOfCylinders`: Determines how many pistons are linked to the crankshaft, impacting power output  
  - `length`: Represents the crankshaft’s length, affecting rotational balance and stability  
  - `material`: Specifies the material used, influencing durability and performance under stress

EngineSystem Class

Fields  
- `motor`: A Motor object responsible for generating the engine’s power  
- `pistons`: A vector of Pistons that work in sync to produce linear force  
- `crankshaft`: A Crankshaft object that converts piston motion into rotation

Methods  
- `ignite()`: Starts the engine and initializes power generation  
- `accelerate()` and `decelerate()`: Control power output by adjusting the motor, impacting the car’s speed  
- `shutdown()`: Stops the engine, halting all power output

System Operation

The EngineSystem operates by generating power that is converted to rotational energy, which is then transmitted to the car’s transmission. 

1. Starting: The motor is ignited, which drives the pistons and crankshaft to begin power generation  
2. Power Control: The engine’s power output can be increased or decreased based on driving conditions  
3. Stopping: Shutting down the engine halts all movement, cutting power to the transmission