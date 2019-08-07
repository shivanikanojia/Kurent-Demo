
kurento-hello-world
===================

Kurento Java Tutorial: Hello World (WebRTC in loopback).

Running this tutorial
---------------------

In order to run this tutorial, please read the following [instructions].

What is Kurento
---------------

Kurento is a WebRTC media server and a set of client APIs making simple the development of advanced video applications for WWW and smartphone platforms. Kurento Media Server features include group communications, transcoding, recording, mixing, broadcasting and routing of audiovisual flows.

Installation
-------------

Make sure that GnuPG is installed
sudo apt-get update \
  && sudo apt-get install --no-install-recommends --yes \
     gnupg
Define what version of Ubuntu is installed in your system
# Run ONLY ONE of these lines:
DISTRO="xenial"  # KMS for Ubuntu 16.04 (Xenial)
DISTRO="bionic"  # KMS for Ubuntu 18.04 (Bionic)
Add the Kurento repository to your system configuration
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 5AFA7A83

sudo tee "/etc/apt/sources.list.d/kurento.list" >/dev/null <<EOF
# Kurento Media Server - Release packages
deb [arch=amd64] http://ubuntu.openvidu.io/6.11.0 $DISTRO kms6
EOF
Install KMS(Kurento Media Server)
sudo apt-get update \
  && sudo apt-get install --yes kurento-media-server
Start/Stop KMS 
sudo service kurento-media-server start
sudo service kurento-media-server stop
