# Simulation of ML-Based Cooling Shroud System

## Overview

The **ML-Based Predictive Cooling Shroud System** is a model-based industrial cooling solution designed to improve thermal management in control cabinets and server enclosures.

Conventional cooling systems generally use fixed-speed fans and reactive temperature thresholds. This project introduces a predictive cooling approach that anticipates future temperature variations and automatically adjusts fan speed and damper position to maintain safe operating conditions while reducing unnecessary energy consumption.

The complete system is modelled and simulated using MATLAB, Simulink, System Composer, and Simscape Multibody.

## Problem Statement

Traditional industrial cooling systems respond only after temperatures exceed predefined limits. This can result in:
- Delayed cooling response.
- Unnecessary fan operation and energy consumption.
- Inefficient airflow distribution.
- Increased risk of overheating and component damage.

**Proposed Solution:** An intelligent predictive cooling system that uses machine learning to estimate future temperatures and dynamically control fan speed and damper angle.

## Project Objectives

- Develop an ML-based temperature prediction model.
- Predict future ambient and server temperature conditions.
- Dynamically regulate fan speed and damper position.
- Model realistic fan and damper mechanical behaviour.
- Implement closed-loop error monitoring and safety feedback.
- Improve thermal stability and energy efficiency.

## System Architecture

The system follows a closed-loop predictive control architecture consisting of:

1. **Temperature Sensing:** Simulates ambient and server temperature inputs.
2. **ML-Based Controller:** Predicts future temperature behaviour and determines the required cooling actions.
3. **Fan and Damper Actuation:** Simulates fan rotation and damper movement using mechanical models.
4. **Error Analyzer:** Compares desired and actual actuator outputs.
5. **Error Feedback:** Generates override signals when actuator errors exceed acceptable limits.
6. **Monitoring System:** Displays temperatures, predictions, actuator outputs, errors, override status, and power consumption.

## Working Principle

1. Ambient and server temperature values are provided as system inputs.
2. Input values are normalized using the parameters obtained during model training.
3. The trained ML model predicts future temperature behaviour.
4. The controller calculates the required fan speed, damper angle, and estimated power consumption.
5. The fan and damper subsystems simulate the corresponding mechanical actions.
6. Actual actuator outputs are compared with desired values.
7. Supervisory feedback identifies deviations and generates override signals when safety limits are exceeded.
8. The monitoring subsystem observes and evaluates overall system performance.

## Machine Learning Model

A function-fitting neural network is used for predictive control.

- Network structure: 2 input neurons, 15 hidden neurons, and 5 output neurons.
- Training and validation are performed in MATLAB.
- Performance is evaluated using Mean Squared Error (MSE), training-state plots, error histograms, and regression plots.
- The trained model is integrated into the Simulink control architecture.

## Technologies Used

| Technology | Purpose |
|---|---|
| MATLAB | ML model development and calculations |
| Simulink | System modelling and simulation |
| System Composer | Modular system architecture |
| Simscape Multibody | Mechanical modelling of fan and damper |
| Neural Networks | Predictive temperature modelling |

## Simulation Results

One of the sample test cases produced the following results:

| Parameter | Value |
|---|---:|
| Ambient Temperature | 23.20 °C |
| Server Temperature | 56.50 °C |
| Predicted Server Temperature | 48.44 °C |
| Fan Speed | 2092 RPM |
| Damper Angle | 44.61° |
| Estimated Fan Power | 11.06 W |

The simulation demonstrates predictive cooling control, coordinated fan and damper actuation, and closed-loop monitoring.

Other observations include:
- Stable actuator response with minimal steady-state error under normal conditions.
- Error feedback detects deviations during rapid temperature variations.
- Override signals provide supervisory safety intervention.
- Fan power consumption varies according to cooling demand.

## Applications

- Industrial automation control cabinets.
- PLC and VFD enclosures.
- Server racks and data centres.
- Telecommunication equipment cabinets.
- Industrial electronic enclosures.
- Edge computing environments.

## Future Scope

- Hardware implementation using microcontrollers or industrial PLCs.
- Integration of multiple temperature sensors for hotspot detection.
- Improved prediction accuracy using advanced ML models.
- IoT-based remote monitoring and data logging.
- Predictive maintenance and real-time industrial deployment.

## Project Type

Academic Practice Project – Mechatronics System Design Lab (2025–26)

**Institution:** KLE Technological University, Hubballi  
**Department:** Automation and Robotics

## Team Members

- Katila Nag
- Bhoomika Hotagi
- Ishwar Sarawad
- Varsha Patil
- Sujal Patil

## Conclusion

The project demonstrates a model-based predictive cooling solution that integrates machine learning, mechanical actuation, and supervisory feedback control. By anticipating temperature variations and dynamically regulating airflow, the proposed system aims to improve thermal stability, energy efficiency, and equipment reliability in industrial enclosures.
