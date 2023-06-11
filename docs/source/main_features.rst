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
This feature allows users to define a threshold that will automatically push BGP configurations (active rule) if the threshold is triggered.

Terms:
  - Thresholds
    A threshold is a set of defined filters and limit to monitor the traffic, and if the traffic is above the limit, it will trigger a static action assigned to the threshold.
  - Static Actions
    A static action is a simplified BGP rules to be executed when a threshold limit is triggered.
  - Active Rules
    A set of BGP rules as a result of threshold triggered a static action.

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

    b. Add a new threshold using the button "Add Threshold" (*area number 1 in the picture above*). This will open up an "Add Threshold" modal.
    c. In the modal, choose which threshold to add, Packet Limit threshold or Connection Limit threshold.
    d. Define:
      - for Connection Limit threshold: which IP address, IP protocol, source port, and destination port to monitor.
      - for Packet Limit threshold: which IP address and packet length to monitor.
    e. Choose a static action to execute when the threshold is triggered, if no static action defined yet, skip to step no. 3 first.
    f. Define how long the action should be executed in the time limit.
    g. Define an additional filter to be pushed along with the static action when the threshold is triggered.
    h. Lastly, enable or disable the threshold, and click the blue "Add" button.

    .. note::
        If the user wants to edit or delete the threshold created, use the edit/delete button at the *area number 2 in the picture above*.
    .. note::
        Filter the Connection Limit threshold or Packet Limit threshold using the filter in *area number 3 in the picture above*.

  3. Define a static action:
    a. Navigate to "Static Actions" section.

    .. figure:: images/static-actions.png
        :align: center

        Static Actions

    b. Add a new static action using the button "Add Static Action" (*area number 1 in the picture above*). This will open up a "Static Action" modal.
    c. In the modal, define the actions (BGP rule) to be taken when a threshold is triggered. The actions available are:
      - block all UDP ports
      - block all TCP ports
      - block all ICMP ports
      - block specific UDP source ports
      - block specific TCP source ports
      - block specific UDP destination ports
      - block specific TCP destination ports
      - block specific packet lengths
      - limit the packet rate
    d. Lastly, enable or disable the static action and click "Add" button on the top right.

    .. note::
        If the user wants to edit or delete the static action created, use the edit/delete button at the *area number 2 in the picture above*.

  4. Check the active rules:
    a. Navigate to "Active Rules" section.

    .. figure:: images/active-rules.png
        :align: center

        Active Rules
    
    b. User can edit/delete the BGP rule from the edit/delete button at the *area number 1 in the picture above*.

    .. note::
        This dashboard will show which active rules are currently created from the threshold triggers.