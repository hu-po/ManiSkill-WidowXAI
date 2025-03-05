# WidowX AI Robot Description (URDF)

this is an un-official model of the Trossen Robotics WidowX AI robot.

the official URDF can be found here: https://github.com/TrossenRobotics/trossen_arm_description

this repo is based off of a similar ManiSkill repo for the WidowX 250S robot: https://github.com/haosulab/ManiSkill-WidowX250S


## Changes Made:

- fixed mesh paths by search replacing `package://trossen_arm_description/meshes` (ROS path) with `meshes` (local path expected by ManiSkill)

- Added a .srdf file for SAPIEN to parse to avoid self collisions for better/faster simulation
- Removed some collision meshes that were unnecessary (e.g. inside another collision mesh)
- Removed mimic joint tags as they are not used and are modelled by the ManiSkill defined controllers