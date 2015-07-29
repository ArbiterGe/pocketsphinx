A simple ROS wrapper for using Pocketsphinx (via gstreamer) with ROS. See docs here http://wiki.ros.org/pocketsphinx

To run on the JetsonBot:

If running on the JetsonBot itself:
$ roslaunch pocketsphinx jetsonbot_voice_cmd.launch

If running remotely:
1. SSH into the JetsonBot and Launch ROS
2. In another Terminal, SSH into the JetsonBot and start a virtual X11 server:
   $ Xvfb :1 &
3. In another Terminal, SSH into the JetsonBot and launch pocketsphinx:
   $ cd ~/jetsonbot
   $ export DISPLAY=:1
   $ roslaunch pocketsphinx jetsonbot_voice_cmd.launch

Note that jetsonbot_voice_cmd.launch is an example file. It has redirected the message cmd_vel. Also, the launch file has a specific mic_input selected, you will have to change this to match your configuration.
