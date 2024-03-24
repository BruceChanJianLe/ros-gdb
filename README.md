# ROS GDB

This repository demonstrates the means to use gdb to debug ROS node.

## Example 1

Using gnome termail!

```xml
    <node pkg="package_name" type="executable_name" name="node_name" output="screen" launch-prefix="gnome-terminal -- gdb -ex run --args">
        <param name="debug" value="$(arg debug)"/>
        <param name="robot_name" value="$(arg robotname)"/>
    </node>
```

Apart from gdp, you can also use Valgrind for memory related issue.

https://valgrind.org/docs/manual/quick-start.html

## Example 2

However, you do not always have the option for gnome terminal. Here is a way to get around with xterm fix font size.
```xml
  <node pkg="move_base" type="move_base" respawn="false" name="move_base" output="screen" launch-prefix="xterm -fa 'Monospace' -fs 14 -e gdb -ex run --args" >
    ...
  </node>
```

https://askubuntu.com/questions/161652/how-to-change-the-default-font-size-of-xterm

## Reference
- ROS GDB: https://www.programmersought.com/article/1271458625/
- VSCODE ROS GDB: https://www.programmersought.com/article/28548719454/
- GDB Tutorial: https://www.youtube.com/watch?v=svG6OPyKsrw
- Cppcon Tutorial: https://www.youtube.com/watch?v=PorfLSr3DDI
