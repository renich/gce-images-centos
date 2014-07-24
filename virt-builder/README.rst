virt-builder
============
This project rocks and it's an easy way to edit a guest and use it.

Requirements
------------
* libguestfs-tools-c
* xz-libs (for the parallel implementation of xzcat to work)

Installation
------------

::

    yum install libguestfs-tools-c xz-libs
    dnf install libguestfs-tools-c xz-libs

Start to build
--------------
# First, setup an account at: https://console.developers.google.com

# Create a Project and configure billing for it. You can get a coupon here: https://cloud.google.com/developers/starterpack/

# Create a Google Storage bucket. 

# Then, you need to install the Google Cloud SDK:

::

    # setup google cloud sdk
    curl https://sdk.cloud.google.com | bash

    # activate google cloud in current shell
    source ~/.bash_profile

    # login (headless server)
    gcloud auth login --no-launch-browser

    # activate it
    source ~/.bash_profile

# Now, set your project

::

    gcloud config set project <my-existing-project>

# Configure the image builder. Don't forget to update the gs variable (google storage)

::

    vim ./build

# Build the image.

::

    ./build

# Login and change the root password; which is: root: centosadminpass
