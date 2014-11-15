# Introduction

This is a simple [Gerrit][0] hook for updating [Redmine][1] with information about what changes
are in Gerrit review.

It parses the commit messages from Gerrit and looks for a Redmine issue in the style
of "#1028".

It then adds a informative message to the Redmine issue about the review URL and other
data. It can also change the status of the issue to indicate that this issue is now
under gerrit review.

Script is tested with Redmine 2.4.1 and Gerrit 2.6.1

# Installation

Put the script in the `$GERRIT_HOME/hooks` directory and edit the script to set the variables at the beginning. If gerrit is installed on a Linux server don't forget to make the script executable. 

If the name of the script is changed from patchset-created to something else don't forget to update the `[Hooks]` section of the `$GERRIT_HOME/etc/gerrit.config` to include `patchsetCreatedHook =  new_script_name`. For more information see the gerrit hooks [documentation][2].

# Logging

All print statements are appended to the `$GERRIT_HOME/logs/error_log`. 

[0]:http://gerrit.googlecode.com
[1]:http://redmine.org
[2]:https://gerrit-review.googlesource.com/Documentation/config-hooks.html
