# PlotJuggler 2.5.0

This is the ARPL fork of PlotJuggler 2.5.0

For installing in Ubuntu18.04, you need the following denpendency 
## How to build (ROS users)

The easiest way to install PlotJuggler is through the command:
 
    sudo apt-get install ros-melodic-plotjuggler 

Nevertheless, if you want to compile it from source, for instance to try the very latest version on the master branch, 
you __must__ build PlotJuggler using __catkin__, otherwise the ROS related plugins will not be included.

Follow these instructions:

    sudo apt-get install qtbase5-dev libqt5svg5-dev libqt5multimedia-dev ros-$ROS_DISTRO-ros-type-introspection
    mkdir -p arpl_ws/src; cd arpl_ws/src
    git clone https://github.com/arplaboratory/PlotJuggler.git 
    cd ..
    catkin build
    source devel/setup.bash
    
You should see the following message at the beginning of the compilation step:

    "PlotJuggler is being built using CATKIN. ROS plugins will be compiled"

Both the executable and the plugins will be created in __ws_plotjuggler/devel/lib/plotjuggler__.

To run the application, use the command:

    rosrun plotjuggler PlotJuggler 


