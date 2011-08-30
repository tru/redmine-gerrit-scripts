This is a simple [Gerrit][0] hook for updating [Redmine][1] with information about what changes
are in Gerrit review.

It parses the commit messages from Gerrit and looks for a Redmine issue in the style
of "#1028".

It then adds a informative message to the Redmine issue about the review URL and other
data. It can also change the status of the issue to indicate that this issue is now
under gerrit review.

Script is tested with Redmine 1.2.1 and Gerrit 2.2.1

Install it in $GERRIT_HOME/hooks and edit the script to set the variables at the beginning.

[0]:http://gerrit.googlecode.com
[1]:http://redmine.org