# ROS GDB

This repository demonstrates the means to use gdb to debug ROS node.

## Example

```xml
    <node pkg="package_name" type="executable_name" name="node_name" output="screen" launch-prefix="gnome-terminal -- gdb -ex run --args">
        <param name="debug" value="$(arg debug)"/>
        <param name="robot_name" value="$(arg robotname)"/>
    </node>
```

Apart from gdp, you can also use Valgrind for memory related issue.

https://valgrind.org/docs/manual/quick-start.html

## Reference
- ROS GDB: https://www.programmersought.com/article/1271458625/
- VSCODE ROS GDB: https://www.programmersought.com/article/28548719454/
- GDB Tutorial: https://www.youtube.com/watch?v=svG6OPyKsrw
- Cppcon Tutorial: https://www.youtube.com/watch?v=PorfLSr3DDI
