#!/bin/bash
# Update the package repository and install required packages
yum update -y
yum install -y amazon-efs-utils
yum install -y nfs-utils

# Create a directory for mounting the EFS
mkdir -p /mnt/efs

# Mount the EFS file system (replace fs-12345678 with your EFS file system ID)
file_system_id=fs-12345678
region=us-east-1
mount_point=/mnt/efs

# Mount the file system
mount -t efs -o tls $file_system_id:/ $mount_point

# Add an entry to /etc/fstab for automatic mounting
echo "$file_system_id:/ $mount_point efs defaults,_netdev 0 0" >> /etc/fstab