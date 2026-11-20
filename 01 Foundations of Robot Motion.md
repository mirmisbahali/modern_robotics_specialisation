# Degrees of Freedom of a Rigid Body (Chapter 2 through 2.1)


# Degrees of Freedom of a Robot (Chapter 2.2)


# Configuration Space (Chapter 2 through 2.2)

> What is configuration Space (C-Space)?
> **Configuration space is the set of all possible configurations (positions and orientation) of a robot.**

**Example 1: A robot arm**
Imagine a robot arm with two rotating joints.
- Joint 1 rotates by angle $\theta_1$
- Joint 2 rotates by angle $\theta_2$
To describe the entire arm's configuration, we only need two numbers
$$\text{q} = (\theta_1, \theta_2)$$
It's configuration space is therefore 2-dimensional (2D).

**Example 2: A mobile robot**
Image a robot moving on a flat floor.
To describe its configuration, we need:
- $x$: horizontal position
- $y$: vertical position
- $\theta$: orientation (which direction it faces)
So:
$$\text{q} = (x, y, \theta)$$
It's configuration is **3-dimensional (3D).**

> [!note]
> The most important concept
> **Degrees of Freedom (DOF) = Dimension of Configuration Space** (for an unconstrained robot).
> A robot with 6 independent joint angles has a 6-dimensional configuration space.
> **Remember:** Configuration space doesn't describe only where the robot is. It describes its *entire configuration using the minimum number of independent coordinates*.

## Configuration Space Topology

> [!note]
> What is Topology in Robotics?
> Topology describes the shape and connectivity of a robot's configuration space (C-space).

In simple terms, topology helps us understand how configurations are connected, especially whether the configuration space has loops or other  special properties.

**Example 1**: A robot moving in a straight line
The robot can move left or right.
- Configuration: $q = x$
- C-Space: a **line** $\mathbb{R}$
- Topology: a line with no loops.

**Example 2**: A rotating robot joint
Imagine a joint that can  rotate continously through 360$\degree$
- Configuration: $q = \theta$
- C-Space: a **circle** $S^1$
- Topology: circular, because $0\degree$ and $360\degree$ represent the same configuration.

**Example 3**: A robot arm with two rotating joints
Each joint has a circular configuration space.
Combining two circles gives us a **torus (donut shape)**.
Mathematically:
$$C = S^1 \times S^1$$
> [!important]
> **Dimension tells us how many independent coordinates we need. Topology tells us how the configuration space is connected and structured.**
> Example: a line and circle are both 1-Dimensional, but they have different topologies. 
> This distinction becomes important when planning robot motions and avoiding obstacles.


## Configuration Space Representation
![[c_space_representation_summary.png]]
![[Configuration Space Representation Summary.png]]

> What is Configuration Space Representation?
> Configuration space representation is the mathematical way we describe all possible configurations of a robot using coordinates.

In *Modern Robotics*, there are four important types of configuration space.

### 1. Euclidean Space ($\mathbb{R}^n$)
Used when a robot has unrestricted linear movement.
Example: A robot moving on a flat surface.
$$q = (x,y)$$
It's configuraiton space is $\mathbb{R}^n$

### 2. Circle ($S^1$)
Used for a joint that can rotate continously.
Example: A rotating robot joint.
$$q = \theta$$
Its configuration space is $S^1$, because $0\degree$ and $360\degree$ represent the same configuration.
### 3. Sphere ($S^2$)
Used to represent directions in 3D space.
Example: A unit vector pointing in any direction.
Its configuration space is $S^2$, the surface of a sphere.

### 4. Special Euclidean Group ($SE(3)$)
Used to describe a rigid robot's complete position and orientation in 3D.

A free-flying robot needs:
- 3 coordinates for position: $x, y, z$
- 3 independent coordinates for orientation.
So it has **6 degrees of freedom**.

Its configuration space is $SE(3)$.

#### Important distinction

| Space          | Dimension | Represents                   |
| -------------- | --------- | ---------------------------- |
| $\mathbb{R}^2$ | 2         | Position on a plane          |
| $S^1$          | 1         | Rotational angle             |
| $S^2$          | 2         | Direction in 3D              |
| $SO(3)$        | 3         | Orientation in 3D            |
| $SE(3)$        | 6         | Position + orientation in 3D |

> [!note]
> **One key idea to remember:** A configuration space can have dimension $n$ without being equivalent to $\mathbb{R}^n$.
> For example, a rotating joint has one DOF, but its configuration space is a circle $S^1$, not a line $\mathbb{R}$.



# Configuration and Velocity Constraints (Chapter 2.4)

Todo: Holonomic contraints, Non-holonomic constraints, Pffaffian constraints.


# Task Space and Workspace (Chapter 2.5)



# Introduction to Rigid-Body Motions (Chapter 3 through 3.1)
![[right_hand_thumb_axes.png]]
![[right_hand_thumb_rule.png]]


## Rotation Matrices (3.2.1)


### Properties of rotation matrices



## Angular Velocities (Chapter 3.2.2)


## Exponential Coordinates of Rotation (Chapter 3.2.3)


# Homogeneous Transformation Matrices (Chapter 3 through 3.3.1)


## Twists (Chapter 3.3.2)


## Exponential Coordinates of Rigid-Body Motion (Chapter 3.3.3)


# Wrenches (Chapter 3.4)



