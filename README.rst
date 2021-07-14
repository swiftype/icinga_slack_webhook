icinga-slack-webhook
==============

A script to send notifications to Slack.com from Nagios or Icinga via the generic webhook integration

.. image:: https://travis-ci.org/alphagov/icinga_slack_webhook.png?branch=master
   :target: https://travis-ci.org/alphagov/icinga_slack_webhook

The `homepage is on Github <https://github.com/alphagov/icinga_slack_webhook>`_

Installation
------------

    $ pip install icinga-slack-webhook

Usage
-----

::

    usage: icinga_slack_webhook_notify [-h] -c CHANNEL -m MESSAGE -s SUBDOMAIN -t TOKEN
                                       [-A SERVICEACTIONURL] [-H HOST] [-L LEVEL]
                                       [--host-state HOST_STATE]
                                       [-M HEADERMESSAGE] [-N SERVICENOTESURL] [-S STATUSCGIURL]
                                       [-U USERNAME]

    Send an Icinga Alert to Slack.com via a generic webhook integration

    optional arguments:
      -h, --help           show this help message and exit
      -c CHANNEL           The channel to send the message to
      -m MESSAGE           The text of the message to send
      -s SUBDOMAIN         Slack.com subdomain
      -t TOKEN             The access token for your integration
      -A SERVICEACTIONURL  An optional action_url for this alert {default: None}
      -H HOST              An optional host the message relates to {default: UNKNOWN}
      --host-state HOST_STATE
                            An optional state the host is in, use this for host alerts
      -L LEVEL             An optional alert level {default: UNKNOWN}
      -M HEADERMESSAGE     A header message sent before the formatted alert
                           {default: I have received the following alert:}
      -N SERVICENOTESURL   An optional notes_url for this alert {default: None}
      -S STATUSCGIURL      The URL of status.cgi for your Nagios/Icinga instance
                           {default: https://nagios.example.com/cgi-bin/icinga/status.cgi}
      -U USERNAME          Username to send the message from {default: Icinga}
      -V                   Display version information
