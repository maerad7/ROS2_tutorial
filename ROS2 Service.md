# ROS Services
- Service are used to communicate between nodes using a client-server model. where the server respondes when the client make a requeest.

1. in a new terminal
<pre>ros2 run turtlesim turtlesim_node</pre>

2. In anorther terminal, run
<pre>ros2 run turtlesim turtle_teleop_key</pre>

3. List all service names
<pre>ros2 service list</pre>
<pre>ros2 service list -t </pre>

4. View service type another way
<pre>ros2 service type service_name</pre>
<pre>ros2 service type /claer</pre>

5. Find service with specific type
<pre>ros2 service find service_type</pre>
<pre>ros2 service find std_srvs/srv/Empty</pre>

6. See interface
<pre>ros2 interface show service_type</pre>
<pre>ros2 interface show turtlesim/srv/Spawn</pre>

7. Caliing a service
<pre>ros2 service call service_name service_type argument</pre>
<pre>ros2 service call /clear std_srvs/srv/Empty</pre>
<pre>ros2 service call /spawn turtlesim/Spawn "{x: 2, y: 2, theta: 0.2, name: ''}"</pre>

