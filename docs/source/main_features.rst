Main Features
=============

IP Statistics
-------------
This feature enables users to monitor Sflow IP statistics and track BGP server's status.

How to access:
  - Log in to your account.
  - From the dashboard, navigate to the "IP Statistics" section.

Actions available:
  - Filter the IP Statistics by UDP Source Ports, UDP Destination Ports, and Unique Connection Threshold in the Settings section, :ref:`connection-limit` part.
  - View unfiltered IP Statistics by typing the destination IP address in the search box.

Manual BGP Rules
----------------
This feature allows users to manually push BGP configurations easily.

How to access:
  - Log in to your account.
  - From the dashboard, navigate to the "Manual Rules" section.

Actions available:
  - Add a BGP rule
  - View current BGP neighbors
  - Filter BGP rules based on destination IP address
  - Edit a BGP rule

.. figure:: images/manual-rules.png
    :align: center

    Manual Rules

Automatic BGP Rules
-------------------
This feature allows users to define a threshold that will automatically push BGP configurations if the threshold is triggered.

There are two kinds of thresholds:
  - Connection Limit threshold
    A connection limit threshold will monitor a specific destination IP address, source ports, and destination ports traffic.
  - Packet Limit threshold
    A packet limit threshold will monitor a specific destination IP address and packet length traffic.

Step-by-step instructions:
  1. Log in to your account.
  2. Define a threshold:
    a. Navigate to "Thresholds" section.

    .. figure:: images/thresholds.png
        :align: center

        Thresholds

    b. Add a new threshold using the button "Add Threshold" (*red square number 1 in the picture above*). This will open up an "Add Threshold" modal.
    c. In the modal, choose which threshold to add, Packet Limit threshold or Connection Limit threshold.
    d. Define:
      - for Connection Limit threshold: which IP address, IP protocol, source port, and destination port to monitor.
      - for Packet Limit threshold: which IP address and packet length to monitor.
    e. Choose a Static Action to execute when the threshold is triggered.
    f. Define how long the action should be executed in the time limit.
    g. Define an additional filter to be pushed along with the Static Action when the threshold is triggered.
    h. Lastly, enable or disable the threshold, and click the blue "Add" button.
    i. The modal will close, and if the user wants to edit or delete the threshold created, use the edit/delete button at the *red square number 2 in the picture above*.
    j. Filter the Connection Limit threshold or Packet Limit threshold using the filter in *red square number 3 in the picture above*.

  3. Define a static action:
    a. Navigate to "Static Actions" section.
  4. Check the active rules:
    a. Navigate to "Active Rules" section.
