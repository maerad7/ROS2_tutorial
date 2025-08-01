# ROS Topic
- A topic is one way data is moved between nodes, where 1 or more publisher nodes can connect to 1 or more subscriber nodes.

1. Open new terminal and run
<pre>ros2 run package_name excutables</pre>
<pre>ros2 run turtlesim turtlesim_node</pre>

2. Open new terminal and run. Move the turtle anywhere(nedded for the rqt graph to show connection later)
<pre>ros2 run turtlesim turtle_teleop_keyt</pre>

3. See list of topics
<pre>ros2 topic list</pre>
<pre>ros2 topic list -t </pre>

4. Start rqt graph. Yncheck hide boxes to see hidden topics.
<pre>rqt_graph<pre>

5. Seetopic output. Move with teleop to see output after running command.
<pre>ros2 topic echo topic_name</pre>
<pre>ros2 topic echo /turtle1/cmd_vel</pre>

6. View topic info
<pre>ros2 topic info topic_name</pre>
<pre>ros2 topci info /turtle1/cmd_vel</pre>

7.See interface definition.
<pre>ros2 interface show type
<pre>ros2 interface show geometry_msgs/msg/Twist</pre>

8. Publish data to a topic("-=once" means publish once and exit)
- x: 2.0 <== 띄어 쓰기 중요.
<pre>ros2 topic pub topic_name msg_target</pre>
<pre>ros2 topic pub --once /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0, y: 0.0, z: 0.0}, angular : {x: 0.0, y: 0.0, z: 1.8}}"</pre>

9. Publish data to a topic with rate 1hz.
<pre>ros2 topic pub --rate 1 /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0, y: 0.0, z: 0.0}, angular : {x: 0.0, y: 0.0, z: 1.8}}"</pre>