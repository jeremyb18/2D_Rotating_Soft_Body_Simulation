# Rolling Soft Body Collision Simulator

This project is a 2D physics simulation that models the collision and rolling of a soft body (a ball) on various surfaces. It goes beyond simple bouncing by incorporating torque and friction to create a more realistic rolling effect. This was developed as a fun way to apply and understand fundamental physics principles from my first semester of college.

---

## Key Features

-   **Soft Body Collisions:** Collisions are modeled using a spring force ($F = -kx$), allowing for control over the "softness" of the interacting objects.
-   **Torque and Friction:** The simulation includes static and kinetic friction to accurately model the transition from sliding to rolling.
-   **Realistic Rolling:** By applying the principles of conservation of energy and moment of inertia, the ball exhibits believable rolling behavior.
-   **Customizable Environment:** You can easily define different surfaces and initial conditions for the ball to interact with.

---

## How It Works

The simulation is built in Python and relies on `numpy` for efficient vector calculations and `matplotlib` for visualization.

### Soft Body Collisions

When the ball collides with a surface, a repulsive force proportional to the depth of penetration is applied. This is analogous to a spring, where the spring constant `k` determines the stiffness of the objects.

### Rolling Friction

To achieve realistic rolling, the simulation calculates the torque exerted by friction. The force of friction is determined by the normal force and the coefficient of friction ($F = \mu N$). This torque then influences the angular acceleration of the ball, causing it to roll. The simulation assumes no slipping occurs once rolling has started.

---

## Getting Started

### Prerequisites

-   Python 3
-   NumPy
-   Matplotlib

### Running the Simulation

1.  Clone this repository.
2.  Run the Jupyter Notebook file `Rotationing_Soft_Body_Project.ipynb`.
3.  The simulation will run, and a plot will be generated showing the path of the ball.

---

## Customization

You can modify the following parameters in the code to see how they affect the simulation:

-   **Ball Properties:** Change the ball's initial position, velocity, radius, mass, and angular velocity in the `ball` class instance.
-   **Surface Geometry:** Modify the `Points` list to create different surfaces for the ball to interact with.
-   **Physical Constants:** Adjust the coefficients of kinetic and static friction (`μk`, `μs`) and the time step (`dt`) to see different physical behaviors.
