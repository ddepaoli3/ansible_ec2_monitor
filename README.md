# ansible_ec2_monitor
Ansible Role to install CloudWatchMonitoringScripts and Monitor Memory and Disk Metrics for Amazon EC2 Linux Instances

Role Variables
--------------

In vars/default.yaml file there are default variables specification.

If the EC2 has no role to send metric and you have an access and secret key override _cron\_specs_ variable as follow:
```
cron_specs:
    -{name: "Name of the task", minute: "*/5", hour: "*", job: "{{cloud_watch_monitoring_path}}/aws-scripts-mon/mon-put-instance-data.pl --disk-space-util --disk-path=/mnt/data --from-cron --aws-access-key-id=AWS_KEY --aws-secret-key=AWS_SECRET_KEY"}
```

Dependencies
------------

This package has no dependencies on modules not included with Ansible by default.

License
-------

Apache

Author Information
------------------

Created by Amrit Singh
https://www.twitter.com/_amrit_
