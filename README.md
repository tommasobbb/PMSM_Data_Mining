# Notebook for Time Series Analysis of a Permanent Magnet Synchronous Motor


**Authors**: Tommaso Baroni, Luca Bestagno

**Dataset**: Electric Vehicle Temperature Dataset


# **Context**

The data set comprises several sensor data collected from a permanent magnet synchronous motor (PMSM) deployed on a test bench. The PMSM represents a german OEM's prototype model. Test bench measurements were collected by the LEA department at Paderborn University.

## **Content**

All recordings are sampled at **2 Hz**. The data set consists of multiple measurement sessions, which can be distinguished from each other by column "profile_id". **A measurement session can be between one and six hours long**.

The motor is excited by hand-designed driving cycles denoting a reference **motor speed** and **a reference torque**.
Currents in d/q-coordinates (columns "i_d" and i_q") and voltages in d/q-coordinates (columns "u_d" and "u_q") are a result of a standard control strategy trying to follow the reference speed and torque.
Columns "motor_speed" and "torque" are the resulting quantities achieved by that strategy, derived from set currents and voltages.

Most driving cycles denote random walks in the speed-torque-plane in order to imitate real world driving cycles to a more accurate degree than constant excitations and ramp-ups and -downs would.

## **Goal**
Our focus will be on predicting the 'stator_winding' temperature. The interdependencies between 'stator_winding', 'stator_yoke', and 'stator_tooth' temperatures suggest that accurate predictions of one can yield significant insights into the others. Furthermore, the 'stator_winding' temperature's correlation with 'pm', representing the rotor temperature, indicates that our predictive model can also enhance our understanding of the rotor's thermal state. By targeting 'stator_winding', we aim to develop a model that offers a comprehensive view of the motor's thermal dynamics.

By predicting stator temperatures, we aim to enable preemptive maintenance actions, enhance the longevity of motors, and ensure safety in applications where temperature spikes could lead to catastrophic failures. The success of this endeavor has the potential to significantly reduce downtime and maintenance costs while optimizing performance in various industrial and vehicular applications.