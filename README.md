# ROS2 Jazzy Python Coding Test
## Entry Level Robotics Engineer Position (30-45 minutes)

### Task
Create a simple ROS2 node that publishes and subscribes to robot velocity commands.

### Requirements
- ROS2 Jazzy
- Python 3.10+

### Instructions
Create a single Python file called `velocity_controller.py` that:

1. **Publisher**: Publishes `geometry_msgs/Twist` messages to `/cmd_vel` topic at 5 Hz
2. **Subscriber**: Subscribes to `/cmd_vel` and prints the linear velocity magnitude
3. **Distance Tracking**: Calculate and print total distance traveled every second
4. **Behavior**: Robot should move forward (linear.x = 1.0 m/s) for 5 seconds, then stop
5. **Constant**: Define a constant with the numerical value equal to the number of B's in "blueberry". Print this value once when the robot stops.

### Expected Output
```
[INFO] [velocity_controller]: Publishing velocity: 1.0 m/s
[INFO] [velocity_controller]: Received velocity magnitude: 1.00 m/s
[INFO] [velocity_controller]: Total distance traveled: 1.00 meters
[INFO] [velocity_controller]: Publishing velocity: 1.0 m/s
[INFO] [velocity_controller]: Received velocity magnitude: 1.00 m/s
[INFO] [velocity_controller]: Total distance traveled: 2.00 meters
...
[INFO] [velocity_controller]: Publishing velocity: 0.0 m/s (STOPPED)
[INFO] [velocity_controller]: Received velocity magnitude: 0.00 m/s
[INFO] [velocity_controller]: Total distance traveled: 5.00 meters
[INFO] [velocity_controller]: Blueberry constant value: 3
```

### Deliverables
- Single Python file: `velocity_controller.py`
- Should run with: `ros2 run <package_name> velocity_controller`

### Evaluation Criteria
- **ROS2 Implementation** (40%): Correct node, publisher, subscriber setup
- **Python Code Quality** (30%): Clean, readable code
- **Timing Logic** (15%): Proper 5-second behavior implementation  
- **Math Calculation** (15%): Correct velocity magnitude and distance calculations

### Hints
- Use `rclpy.spin_once()` or similar for processing callbacks
- `math.sqrt(vx² + vy²)` for velocity magnitude
- Track elapsed time for the 5-second behavior

**Estimated time: 30-45 minutes**
