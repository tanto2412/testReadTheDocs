Settings
========

Website Name
------------
This setting is for changing the name of the website's name and title.

+---------------+-----------------+-------------------------------+
| Field         | Sample Data     | Description                   |
+===============+=================+===============================+
| Web Site Name | DDoS Mitigation | The title/name of the website |
+---------------+-----------------+-------------------------------+

Database Settings
-----------------
This setting is for configuring the parameters of the MySQL database.

+----------+-------------+---------------------+
| Field    | Sample Data | Description         |
+==========+=============+=====================+
| DB Name  | test        | MySQL database name |
+----------+-------------+---------------------+
| Host     | localhost   | MySQL hostname      |
+----------+-------------+---------------------+
| Port     | 3306        | MySQL port          |
+----------+-------------+---------------------+
| Username | root        | MySQL username      |
+----------+-------------+---------------------+
| Password | root        | MySQL password      |
+----------+-------------+---------------------+

SMTP Settings
-------------
This setting is for configuring the SMTP used for sending email after registration.

+----------+------------------+------------------------------+
| Field    | Sample Data      | Description                  |
+==========+==================+==============================+
| Protocol |                  | SMTP protocol used           |
+----------+------------------+------------------------------+
| Host     | smtp.mailtrap.io | SMTP hostname                |
+----------+------------------+------------------------------+
| Port     | 2525             | SMTP port                    |
+----------+------------------+------------------------------+
| Username | user             | SMTP email provider username |
+----------+------------------+------------------------------+
| Password | password         | SMTP email provider password |
+----------+------------------+------------------------------+

Reports Settings
----------------
This setting is for configuring how the Sflow data received and shown.

+----------+-------------+----------------------------------------------+
| Field    | Sample Data | Description                                  |
+==========+=============+==============================================+
| Port     | 6343        | Port to listen Sflow data sent by BGP server |
+----------+-------------+----------------------------------------------+
| Interval | 10000       | Interval to refresh IP Statistics page       |
+----------+-------------+----------------------------------------------+

.. _connectionlimit:

Connection Limits
-----------------
This setting is for configuring the filter of data shown on IP Statistics page.

+-----------------------------+---------------------------------------------+-------------------------------------------------------------------+
| Field                       | Sample Data                                 | Description                                                       |
+=============================+=============================================+===================================================================+
| Interval in seconds         | 3600                                        | Sflow data retention period                                       |
+-----------------------------+---------------------------------------------+-------------------------------------------------------------------+
| UDP source port             | 16,53,123,389,161,1194,1900,3283,3702,11211 | UDP source ports to be detected in the IP statistics              |
+-----------------------------+---------------------------------------------+-------------------------------------------------------------------+
| UDP destination port        | 25565,25566                                 | UDP destination ports to be detected in the IP statistics         |
+-----------------------------+---------------------------------------------+-------------------------------------------------------------------+
| Unique connection threshold | 300                                         | The minimum unique connections count to be shown in IP Statistics |
+-----------------------------+---------------------------------------------+-------------------------------------------------------------------+
| Connection rate in seconds  | 100                                         | The period to calculate the unique connections (in seconds)       |
+-----------------------------+---------------------------------------------+-------------------------------------------------------------------+