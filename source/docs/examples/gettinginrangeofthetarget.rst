Getting in Range of the Target
==============================

Knowledge and Equipment Needed
-----------------------------------------------

- Everything required in :ref:`Aiming at a Target <docs/examples/aimingatatarget:Knowledge and Equipment Needed>`.
- Large space where your robot can move around freely

Code
-------

In FRC, a mechanism usually has to be a certain distance away from it’s target in order to be effective and score. In the last example, we showed how to aim your robot at the target. Now you will learn how to move to a certain distance from the target. In order to properly complete this example, ensure that your robot is pointed towards the target, but this will not be necessary in the future. This example is similar to the previous one and will also be using the P term of the PID loop and PhotonLib, specifically the distance function of PhotonUtils. While the operator holds down a button, the robot will drive towards the target and get in range.

.. warning:: The PhotonLib utility to calculate distance depends on the camera being at a different vertical height than the target. If this is not the case, a different method for estimating distance, such as target width or area, should be used. In general, this method becomes more accurate as range decreases and as the height difference increases.

.. note:: There is no strict minimum delta-height necessary for this method to be applicable, just a requirement that a delta exists.

The following example is from the PhotonLib example repository (`Java <https://github.com/PhotonVision/photonvision/tree/master/photonlib-java-examples/src/main/java/org/photonlib/examples/getinrange>`_/`C++ <https://github.com/PhotonVision/photonvision/tree/master/photonlib-cpp-examples/src/main/cpp/examples/getinrange>`_).

.. tab-set::

    .. tab-item:: Java

       .. rli:: https://raw.githubusercontent.com/PhotonVision/photonvision/master/photonlib-java-examples/src/main/java/org/photonlib/examples/getinrange/Robot.java
         :language: java
         :linenos:

    .. tab-item:: C++ (Header)

       .. rli:: https://raw.githubusercontent.com/PhotonVision/photonvision/master/photonlib-cpp-examples/src/main/cpp/examples/getinrange/include/Robot.h
         :language: c++
         :linenos:

    .. tab-item:: C++ (Source)

       .. rli:: https://raw.githubusercontent.com/PhotonVision/photonvision/master/photonlib-cpp-examples/src/main/cpp/examples/getinrange/cpp/Robot.cpp
         :language: c++
         :linenos:

.. hint:: The accuracy of the measurement of the camera's pitch (:code:`CAMERA_PITCH_RADIANS` in the above example), as well as the camera's FOV, will determine the overall accuracy of this method.
