# mautic-cron-jobs
Cron jobs for mautic 5

         2 * * * *     php /var/www/html/bin/console mautic:segments:update > /var/log/cron.pipe 2>&1
         3 * * * *     php /var/www/html/bin/console mautic:campaigns:rebuild > /var/log/cron.pipe 2>&1
         5 * * * *     php /var/www/html/bin/console mautic:campaigns:trigger > /var/log/cron.pipe 2>&1
         * 1 * * *  php /var/www/html/bin/console mautic:custom-field:create-column
         1 * * * * php /var/www/html/bin/console messenger:consume email
         2 * * * * php /var/www/html/bin/console mautic:email:fetch

# cyberpanel cron-jobs

         2 * * * * /usr/local/lsws/lsphp81/bin/php /home/talent-logic.com/public_html/bin/console mautic:segments:update 
         3 * * * *     /usr/local/lsws/lsphp81/bin/php /var/www/html/bin/console mautic:campaigns:rebuild > /var/log/cron.pipe 2>&1
         5 * * * *     /usr/local/lsws/lsphp81/bin/php /var/www/html/bin/console mautic:campaigns:trigger > /var/log/cron.pipe 2>&1
         * 1 * * *  /usr/local/lsws/lsphp81/bin/php /var/www/html/bin/console mautic:custom-field:create-column
         1 * * * * /usr/local/lsws/lsphp81/bin/php /var/www/html/bin/console messenger:consume email
         2 * * * * /usr/local/lsws/lsphp81/bin/php /var/www/html/bin/console mautic:email:fetch
