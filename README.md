# PID
This project implements a PID controller for keeping the car on track by appropriately adjusting the steering angle.
  
#### What's a PID controller

A **proportional–integral–derivative controller** (PID controller) is one of the most common control loop feedback mechanisms. A PID controller continuously calculates an **error function** (which in our case is the distance from the center of the lane) and applies a correction based on proportional (P), integral (I), and derivative (D) terms.

#### Choosing PID Parameters
The behavior of a PID controller depends on three main parameters, namely the **proportional**, **integral** and **derivative gain**. Each one of these three parameters controls the strenght of the respective controller's response. In particular:
1. **Proportional gain** regulates how large the change in the output will be for a given change in the error. If the proportional gain is too high, the system can become unstable (see *p controller* gif above).
2. **Integral gain** contributes in proportion to both the magnitude of the error and the duration of the error. In this way controller is able to eliminate the residual steady-state error that occurs with a pure proportional controller (*i.e.* a purely proportional controller operates only when error is non-zero) and is able to deal with systematic biases.
3. **Derivative gain** decides how much the error's rate of change is taken into account when computing the response. In other words, if the desired setpoint is getting closer (= error is decreasing) the response must be smoothed in order not to overshoot the target. Derivative component benefits the system's stability and settling time.




