<html>
    <body>
        <script type='text/javascript'>
            function initEmbeddedMessaging() {
                try {
                    embeddedservice_bootstrap.settings.language = 'en'; // For example, enter 'en' or 'en-US'
        
                    embeddedservice_bootstrap.init(
                        '00D7d000008qeja',
                        'CRC_Miaw',
                        'https://grupoboticario--devcrcmiaw.sandbox.my.site.com/ESWCRCMiaw1677876722502',
                        {
                            scrt2URL: 'https://grupoboticario--devcrcmiaw.sandbox.my.salesforce-scrt.com'
                        }
                    );
                } catch (err) {
                    console.error('Error loading Embedded Messaging: ', err);
                }
            };
    	</script>
    	<script type='text/javascript' src='https://grupoboticario--devcrcmiaw.sandbox.my.site.com/ESWCRCMiaw1677876722502/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'>
    	</script>
    </body>
</html>
