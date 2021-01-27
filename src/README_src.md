SO we can have many ROS packages part of one project.

each need to be its own ```git``` repo and will be placed in the src folder by the ```wstool up``` cammand (see main readme in parent folder)

if you want to add a new package see [HERE](http://wiki.ros.org/Packages)
and [HERE](http://wiki.ros.org/ROS/Concepts)

if you want to [make package from scratch](http://wiki.ros.org/ROS/Tutorials/CreatingPackage)


after you make/add one you you need to make sure the folder is not on this git  (this is best practice)

to do this you must add the new pakage foldere to the  ```.gitignore``` file in the parent directory.

    devel/
    build/

    src/low_level_control
    src/dummy_planner
    src/high_level_control
    src/setup_and_launch
    src/topology_emulator
    src/turtle
    src/<MY_NEW_PACKAGE>