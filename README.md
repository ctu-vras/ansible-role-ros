# Ansible Role: ROS

Ansible Galaxy: [ctu_vras.ros](https://galaxy.ansible.com/ui/standalone/roles/ctu_vras/ros/)

Installs the Robot Operating System (ROS) on Ubuntu linux servers. It supports both ROS 1 and ROS 2 distros.

When you run the role twice, you can even get concurrent installations of e.g. ROS 1 One + ROS 2 Jazzy.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    ros_release: Defaults to the default ROS(2) version for the Ubuntu version. If no default is found, defaults to 'noetic'
    ros_version: Defaults to "1" for ROS 1 distros and "2" for ROS 2 distros. You should not change this value.
    ros_package: "ros-base"
    ros_apt_uri: "http://packages.ros.org/ros/ubuntu" for ROS 1 and "http://packages.ros.org/ros2/ubuntu" for ROS 2, or a mirror address
    ros_apt_key_filename: "/usr/share/keyrings/ros(2)-archive-keyring.gpg" for official ROS releases, "/etc/apt/keyrings/ros-one-keyring.gpg" for ROS One
    ros_one_apt_key: "https://ros.packages.techfak.net/gpg.key" (only used for ROS One)
    ros_apt_mirror_filename: For ROS 1 distros, defaults to 'ros-mirror'; for ROS 2 distros, defaults to 'ros2-mirror'. Only used when using a non-default mirror.

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
