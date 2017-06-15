# How To Unsubscribe Someone From Our Mailing Lists

We get unsubscribe requests mostly from folks on local Google Groups mailing lists, but they may also be subscribed to sendy. We need to make sure we unsubscribe them from any DxE mailing lists.
 
 
 
To unsubscribe somebody, first clone the private repo and set up the “mailinglist-membership” command line app:

``` 
git clone git@github.com:directactioneverywhere/private
cd private
git submodule init # initialize the ‘config’ submodule, which has
                   # the secret keys needed. If this doesn’t work,
                   # ask to be given permission to use the config repo
cd mailinglist-membership
pip install -r requirements.txt
python google_groups_cli.py delete_member -e <their-email-address>
```
 
Deleting gmail addresses is fast, but deleting non-gmail addresses is slow (to work around a bug on Google’s side, where you can only delete from all lists if the email is associated with a Google account).

The command will print out all the email lists the person was unsubscribed from.
 
Then, log into sendy and search for their email under “All lists”, and make sure it’s unsubscribed: https://sendy.dxetech.org/list?i=1
 
**NOTE:** If the user’s email was not subscribed to any mailing lists, then ask them if they have any alternate emails.
 
Finally, follow up the user and tell them they’ve been unsubscribed, and to ping us if they get any more DxE emails.
