# wazuh-ntop
Integrate ntopng into Wazuh

Here you will find decoders and rules to integrate ntopng (via Syslog) into Wazuh.

The decoders and rules work with with either text or ECS log format, please only install one of them:

TEXT:

wget https://raw.githubusercontent.com/mimugmail/wazuh-ntop/refs/heads/main/rules/ntopng_text_rules.xml -o /var/ossec/etc/rules/ntopng_text_rules.xml

wget https://raw.githubusercontent.com/mimugmail/wazuh-ntop/refs/heads/main/decoders/ntopng_text_decoder.xml -o /var/ossec/etc/decoders/ntopng_text_decoder.xml

ECS:

wget https://raw.githubusercontent.com/mimugmail/wazuh-ntop/refs/heads/main/rules/ntopng_ecs_rules.xml -o /var/ossec/etc/rules/ntopng_ecs_rules.xml

wget https://raw.githubusercontent.com/mimugmail/wazuh-ntop/refs/heads/main/decoders/ntopng_json_decoder.xml -o /var/ossec/etc/decoders/ntopng_json_decoder.xml

After this, restart wazuh with:
/var/ossec/bin/wazuh-control restart

To configure Wazuh getting syslog alerts please follow the official documentation:
https://documentation.wazuh.com/current/user-manual/capabilities/log-data-collection/syslog.html
