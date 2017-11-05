.. |labmodule| replace:: 1
.. |labnum| replace:: 4
.. |labdot| replace:: |labmodule|\ .\ |labnum|
.. |labund| replace:: |labmodule|\ _\ |labnum|
.. |labname| replace:: Lab\ |labdot|
.. |labnameund| replace:: Lab\ |labund|

Lab |labmodule|\.\ |labnum|\: Install Logstash
----------------------------------------------

Install Logstash

Task 1 - Install Logstah
^^^^^^^^^^^^^^^^^^^^^^^^

#Install Logstash
sudo apt-get install logstash

#Install Additional Plugin (This step can take a while be patient)
 cd /usr/share/logstash/bin/
./logstash-plugin install logstash-filter-translate

#Copy or Create .csv files for application and category searching
/user/local/share/

#Copy config file to logstash_main.conf or create new file
#Directory /etc/logstash/conf.d/
sudo cp logstash_main.conf /etc/logstash/conf.d/logstash.conf

#Logstash restart
sudo systemctl restart logstash.service

#To configure Logstash to start automatically when the system boots up, run the following commands:
sudo /bin/systemctl daemon-reload
sudo /bin/systemctl enable logstash.service

#Logstash Control
sudo systemctl start logstash.service
sudo systemctl stop logstash.service
sudo systemctl status logstash.service

   Example output:

   .. code::


        [snops@f5-super-netops] [~/f5-postman-workflows/local] $ f5-newman-wrapper Wrapper_Demo_1.json
        [Wrapper_Demo_1-2017-03-30-04-08-12] starting run
        [Wrapper_Demo_1-2017-03-30-04-08-12] [runCollection][Authenticate to BIG-IP] running...
        newman


#. Examine the environment variables that were saved at the end of the
   run by executing ``cat Wrapper_Demo_1-env.json``

   Example output:

   .. code-block:: json
      :linenos:
      :emphasize-lines: 29-38

      {
        "id": "c0550892-36d4-4412-bf35-a1d9aa8d2efe",
        "values": [
          {
            "type": "any",
            "value": "10.1.1.4",
            "key": "bigip_mgmt"
          },
          {
            "type": "any",
            "value": "admin",
            "key": "bigip_username"
          },
          {
            "type": "any",
            "value": "admin",
            "key": "bigip_password"
          },
          {
            "type": "any",
            "value": "WYKIVPHCNASNVEC55ZDVNH5OO2",
            "key": "bigip_token"
          },
          {
            "type": "any",
            "value": "1200",
            "key": "bigip_token_timeout"
          },
          {
            "type": "any",
            "value": "12.1.1",
            "key": "bigip_version"
          },
          {
            "type": "any",
            "value": "1.0.196",
            "key": "bigip_build"
          }
        ]
      }

Notice that the ``bigip_version`` and ``bigip_build`` variables were
saved, similar to how this was shown in the Postman GUI Environment Variables.
This file is JSON formatted and can easily be used directly
by other tools to drive further automation.
