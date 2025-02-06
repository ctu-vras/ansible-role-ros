# Ansible Role: ROS

Ansible Galaxy: [ctu_vras.ROS](https://galaxy.ansible.com/ui/standalone/roles/ctu_vras/ROS/)

Installs the Robot Operating System (ROS) on Ubuntu linux servers. It supports both ROS 1 and ROS 2 distros.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    ros_release: Defaults to the default ROS(2) version for the Ubuntu version. If no default is found, defaults to 'noetic'
    ros_version: Defaults to "1" for ROS 1 distros and "2" for ROS 2 distros. You should not change this value.
    ros_package: "ros-base"
    ros_apt_uri: "http://packages.ros.org/ros/ubuntu" for ROS 1 and "http://packages.ros.org/ros2/ubuntu" for ROS 2
    ros_apt_key: "https://raw.githubusercontent.com/ros/rosdistro/master/ros.key"
    ros_apt_key_filename: "/usr/share/keyrings/ros-archive-keyring.gpg"
    ros_apt_repo_filename: For ROS 1 distros, defaults to 'ros-latest'; for ROS 2 distros, defaults to 'ros2'

## Dependencies

None.

## Example Playbook

    - hosts: server
      roles:
        - { role: ctu-vras.ros }

## License

BSD

## Author Information

This role was created in 2015 by [Jamie Alessio](https://github.com/jalessio) and updated in 2025 by [Martin Pecka](https://github.com/peci1).
