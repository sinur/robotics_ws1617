# Robotics WS 16/17
__Group Pingu 🐧__
__Assignment: 2__

|  Name                      | MatrikelNr.   | Mail                       |
|----------------------------|---------------|----------------------------|
| Larissa Zech               | 4594149       | larissa.zech@fu-berlin.de  |
| Niels Groth                | 4573930       | niels.groth@fu-berlin.de   |
| Alexander Hinze-Hüttl      | 4578322       | hinze.alex@gmail.com       |


## 1.

## 2.

$R_{\alpha,\beta,\gamma} = R_x(\alpha) * R_x(\beta) * R_z(\gamma)$

$ =
\begin{pmatrix}
  1 & 0 & 0 \\
  0 & \cos(\alpha) & -\sin(\alpha)\\
  0 & \sin(\alpha) & \cos(\alpha)
 \end{pmatrix} *
 \begin{pmatrix}
   \cos(\beta) & 0 & \sin(\beta) \\
   0 & 1 & 0\\
   -\sin(\beta) & 0 & \cos(\beta)
  \end{pmatrix} *
  \begin{pmatrix}
    \cos(\gamma) & - \sin(\gamma) & 0 \\
    \sin(\gamma) & \cos(\gamma) & 0\\
    0 & 0 & 1
   \end{pmatrix}
$

$
= \begin{pmatrix}
 \cos(\beta) * \cos(\gamma) & -cos(\beta) * \sin(\gamma) & \sin(\beta) & 0
 \\
 \cos(\alpha) * \sin(\gamma)  +
 \sin(\alpha) * \sin(\alpha) * \sin(\beta) & \cos(\gamma) + \cos(\alpha) * \cos(\gamma) - \sin(\alpha) - \sin(\beta) * \sin(\gamma) & -\sin(\alpha) * \cos(\beta) & 0
 \\
 \sin(\alpha) * \sin(\gamma) - \cos(\alpha) * \sin(\beta) * \cos(\gamma) & \sin(\alpha) * \cos(\gamma) + \cos(\gamma) * \sin(\beta) * \sin(\gamma) & \cos(\alpha) * \cos(\beta) & 0
 \\
 0 & 0 & 0 & 1
\end{pmatrix}
$



## 3.
