# Chapter 2: Core Concepts of ROS 2

This chapter will introduce you to the core concepts of the Robot Operating System (ROS) 2. ROS 2 is a set of software libraries and tools that help you build robot applications. It is a complete rewrite of ROS 1, designed to be more robust, secure, and scalable.

## Nodes, Topics, Services, and Actions

These are the fundamental building blocks of any ROS 2 application.

### Nodes

A **node** is a process that performs computation. In ROS 2, a single executable can contain one or more nodes. Nodes are responsible for a specific task, such as controlling a motor, reading a sensor, or planning a path.

### Topics

**Topics** are named buses over which nodes exchange messages. Topics are one-to-many communication channels: a node can publish messages to a topic, and any number of nodes can subscribe to that topic to receive the messages.

### Services

**Services** are a request/response type of communication. One node offers a service, and another node can call that service. Services are a two-way communication channel, where the client sends a request and the server sends a response.

### Actions

**Actions** are similar to services, but they are designed for long-running tasks. Actions provide feedback on the progress of the task, and they can be preempted (cancelled).

## ROS 2 Architecture and Ecosystem

### The ROS 2 Graph

The ROS 2 **graph** is the network of ROS 2 nodes and how they communicate with each other. The graph can be visualized using tools like `rqt_graph`.

### The ROS 2 Ecosystem

The ROS 2 ecosystem is a collection of tools and libraries that help you build robot applications. Some of the most important tools are:

*   **`colcon`**: The build tool for ROS 2.
*   **`rqt`**: A graphical user interface for inspecting and interacting with ROS 2 systems.
*   **`rviz2`**: A 3D visualization tool for ROS 2.
*   **Gazebo**: A 3D robotics simulator.

## Setting Up Your ROS 2 Environment

### Installation

To get started with ROS 2, you need to install it on your system. The official installation instructions can be found on the ROS 2 website. We recommend installing the latest LTS (Long Term Support) release.

### Creating a Workspace

A ROS 2 **workspace** is a directory where you can create and manage your ROS 2 packages. To create a workspace, you need to create a directory and a `src` subdirectory.

```bash
mkdir -p ros2_ws/src
cd ros2_ws
```

### Sourcing the Setup File

Before you can use your ROS 2 workspace, you need to source the setup file. This will add the workspace to your environment.

```bash
source /opt/ros/humble/setup.bash
```

Now you are ready to start building your first ROS 2 application!
