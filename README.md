# certbot-renew.sh
<pre>
#!/bin/bash
#
# Supposing you have /etc/letsencrypt/cli.ini config file with domains
#
# Put this script in a daily cron and your cert will be automagically updated 30 days before expiration.
# If renew doesn't succeed, you'll receive email notification from your CA.
# e.g cron   5 4 * * 2 /etc/certbot-renew.sh > /dev/null 2>&1
# https://certbot.eff.org/docs/using.html#renewal
#
sudo certbot renew --noninteractive --post-hook "service apache2 reload"
# EOF
</pre>
