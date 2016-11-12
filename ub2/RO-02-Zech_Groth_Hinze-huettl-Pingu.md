# Robotics WS 16/17 - Group _Pingu_ 🐧

__Assignment: 2__

|  Name                      | MatrikelNr.   | Mail                       |
|----------------------------|---------------|----------------------------|
| Larissa Zech               | 4594149       | larissa.zech@fu-berlin.de  |
| Niels Groth                | 4573930       | niels.groth@fu-berlin.de   |
| Alexander Hinze-Hüttl      | 4578322       | hinze.alex@gmail.com       |

## 1. Coordinate Transformation
### a)

__rotation and translation matrices:__

$
T_1 = \begin{pmatrix}
  1 & 0 & L_1\\
  0 & 1 & 0\\
  0 & 0 & 1
\end{pmatrix}
$

$ R_1 =
 \begin{pmatrix}
  \cos -\theta_1 & -\sin -\theta_1 & 0\\
  \sin -\theta_1 & \cos -\theta_1 & 0\\
  0 & 0 & 1
\end{pmatrix}
$

$
R_2 = \begin{pmatrix}
 \cos \theta_2 & -\sin \theta_2 & 0\\
 \sin \theta_2 & \cos \theta_2 & 0\\
 0 & 0 & 1
\end{pmatrix}
$

$ T_2 = \begin{pmatrix}
  1 & 0 & L_2\\
  0 & 1 & 0\\
  0 & 0 & 1
\end{pmatrix}
$

* $(x_1,y_1,w_1)^T = R_1 * T_1 * (x,y,1)^T$
$(x_2,y_2,w_2)^T = R_2 * T_2 (x_1,y_1,w_1)^T$


* $x_1 = x * \cos(-\theta_1) - y * \sin(-\theta_1) + L_1*1$
$y_1 = x * \sin(-\theta_1) + y * \cos(-\theta_1)$


* $x_2 = x_1 * \cos(-\theta_2) - y_1 * \sin(-\theta_2) + L_2$
$y_2 = x_1 * \sin(-\theta_2) + y_1 * \cos(-\theta_2)$

### b)
__Partial derivative respect to $\theta_1$__
where $\theta_2,x,y$ are constants:
* $x_1'(\theta_1) = -x*\sin(-\theta_1) - y*\cos(-\theta_1)$
$y_1'(\theta_1) = x*\cos(-\theta_1) - y*\sin(-\theta_1)$


* $x_2'(\theta_1) = x_1'(\theta_1) * \cos(-\theta_2) - y_1'(\theta_1) * \sin(-\theta_2)$
$y_2'(\theta_1) = x_1'(\theta_1) * \sin(-\theta_2) + y_1'(\theta_1)* \cos(-\theta_2)$

__Partial derivative respect to $\theta_2$:__
where $\theta_1,x_1,y_1$ are constants:
* $x_2'(\theta_1) = - x_1 * \sin(-\theta_2) - y_1 * \cos(-\theta_2)$
$y_2' = x_1 * \cos(-\theta_2) - y_1 * \sin(-\theta_2)$


## 2. Rotation Matrix as an Operator
### a)
3D-Rotation matrix has $3\times3$ values. The matrix is defined by three angles _pitch,yaw_ and _roll_. Each value $r_{xy}$ is defined by these angles combined with trigonomic functions:
![](http://msl.cs.uiuc.edu/planning/img822.gif)
* You can choose three random angles to calculate $R$.
* You can choose three random $r$ values when their calculation contain all three angles, to derive the angles step step. Eg:
  * $\beta = \sin^{-1}(-r_{13})$
  * $\gamma = \sin^{-1}(\frac{r_{23}}{\cos(\beta)})$
  * $\alpha = \cos^{-1}( \frac{r_{11}}{\cos(\beta)} )$

### b)

### c)

## 3. Working with the Car
### a)
1. Turn the car on. Press the green button twice.
2. Export all vars to terminal (see README.md)
3. Start roscore?
4. List all topics `rostopic list` make sure you see `/manual_control/speed`
5. run `rqt_graph` to start the graph and add `/motor_control/twist/linear/x` as topic.
6. change motor speed: `rostopic pub manual_control/speed std_msgs/Int16 '{data: 500}'`
7. screenshot plot

### b)
