<html>
    <body>
        <script type='text/javascript'>
            function initEmbeddedMessaging() {
                try {
                    embeddedservice_bootstrap.settings.language = 'pt_BR';

                    window.addEventListener("onEmbeddedMessagingReady", () => {

                        embeddedservice_bootstrap.userVerificationAPI.setIdentityToken({
                        identityTokenType : "JWT", identityToken : "tokenJWT"});

                        console.log("onEmbeddedMessagingReadyQDBUAT>> ");
                    });

                    embeddedservice_bootstrap.init(
                        '00D3B000000IPck',
                        'CRC_QuemDisseBerenice',
                        'https://grupoboticario--uat.sandbox.my.site.com/ESWCRCMiawQDB1684273993056',
                        {
                            scrt2URL: 'https://grupoboticario--uat.sandbox.my.salesforce-scrt.com'
                        }
                    );
                } catch (err) {
                    console.error('Error loading Embedded Messaging: ', err);
                }
            };

            function onUserLogout() {
                embeddedservice_bootstrap.userVerificationAPI
                    .clearSession()
                    .then(() => {
                        console.log("User Logout.");
                    })
                    .catch((error) => {
                        console.log("User Logout Error.");
                    })
                    .finally(() => {
                        
                    });
            }
        </script>
        <script type='text/javascript' src='https://grupoboticario--uat.sandbox.my.site.com/ESWCRCMiawQDB1684273993056/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
    </body>
</html>
