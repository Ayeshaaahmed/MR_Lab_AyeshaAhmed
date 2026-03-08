# Week 1 Answers

## 1. Define the following terms: node, topic, package, workspace.

**Node:**  
A node is a running program in ROS 2 that performs a specific task. Each node usually focuses on one responsibility such as reading sensor data, controlling a robot actuator, or processing information. Nodes communicate with each other to form a complete robotic system.

**Topic:**  
A topic is a communication channel used by ROS 2 nodes to exchange messages. One node can publish data to a topic, while other nodes subscribe to the same topic to receive that data. This publish–subscribe model allows different parts of the system to communicate without being tightly connected.

**Package:**  
A package is the basic organizational unit in ROS 2. It contains source code, configuration files, dependencies, and other resources needed to build and run a particular functionality. Packages help organize projects into manageable components.

**Workspace:**  
A workspace is the main directory where ROS 2 development takes place. It contains multiple packages along with build, install, and log folders that are generated when compiling the code. Developers use the workspace to build, test, and run their ROS 2 applications.

---

## 2. Explain why sourcing is required. What happens if you do not source a workspace?

Sourcing a workspace configures the environment variables so that the system can locate ROS 2 packages, libraries, and executables. It tells the terminal where the built packages are stored and allows ROS commands like `ros2 run` to work properly.  
If the workspace is not sourced, ROS 2 will not recognize newly created packages or nodes, and commands may return errors such as “package not found”.

---

## 3. What is the purpose of `colcon build`? What folders does it generate?

The `colcon build` command is used to compile and build all ROS 2 packages inside a workspace. It prepares the code so that it can be executed by ROS 2 tools. During this process, several folders are automatically created:

- **build/** – contains intermediate build files
- **install/** – stores the final built packages and executables
- **log/** – contains logs of the build process for debugging

These folders help ROS 2 manage the build process and execution environment.

---

## 4. In your own words, explain what the `entry_points` console script does in `setup.py`.

The `entry_points` section in `setup.py` defines executable commands for ROS 2 Python packages. It connects a command name (for example `simple_node`) with the Python function that should run when the command is executed. This allows users to start a node easily using a command like:
## 5b. Publisher–Subscriber Communication Diagram

In ROS 2, nodes communicate with each other using a publish–subscribe model. 
A publisher node sends messages to a topic, and a subscriber node listens to that topic to receive the messages. 
This design allows nodes to communicate without needing direct connections to each other.

Example Diagram:

        +-----------------+
        |  Publisher Node |
        | (publishes data)|
        +-----------------+
                 |
                 |   Topic: /example_topic
                 v
        +-----------------+
        | Subscriber Node |
        | (receives data) |
        +-----------------+

Explanation:
The publisher continuously sends messages to the topic `/example_topic`. 
Any subscriber that is listening to this topic will receive the messages and can process them accordingly.
