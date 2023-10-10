<html>
    <body>
        <script type='text/javascript'>
            function initEmbeddedMessaging() {
                try {
                    embeddedservice_bootstrap.settings.language = 'pt_BR';

                    var token = 'eyJraWQiOiIxMjM0NSIsImFsZyI6IlJTMjU2In0.eyJpc3MiOiJ0ZXN0SXNzdWVyIiwic3ViIjoidXNlcjEiLCJleHAiOjE2ODE0MzAzNjYsImlhdCI6MTY4MTQyNDM2Nn0.jXw6aYFXNJOWntkHMiHw_5h-u-Ic-jhLJG_TzgdbXoJPE3PvCzEi5U1icfQygEdNfwv1Uw04dVnMPBrkB0hEP-kKM1Ot9LidQAv9DHlj9Ns9PJSePUF3xmFUYpBkeUt5Wvw8ag6f-_LGhjciy0W8xHYXHaDwWohnj9TaJ1sR_A3ZNjoZBWq6kVM5szQCFdg_AC_bwSw488OhneYifi2bZMYEPJ7iAh-FPGeAOOp7XRbdPWB8vbqBjfwKHDNFuj1L6SkQ3svwvqPwrh3iHDokm8sT6AkjK0ntAWME01duWC9RLcqrI6E87gBaq86dFBrSTTtZ2JwbBiqfUNfO2S9Y9w';

                    window.addEventListener("onEmbeddedMessagingReady", () => {

                        embeddedservice_bootstrap.userVerificationAPI.setIdentityToken({
                            identityTokenType : "JWT", identityToken : token});

                        console.log("onEmbeddedMessagingReadyTkn>> ");
                    });

                    embeddedservice_bootstrap.init(
                        '00D3B000000IPck',
                        'CRCMiawQDB',
                        'https://grupoboticario--uat.sandbox.my.site.com/ESWCRCMiawQDB1684273993056',
                        {
                            scrt2URL: 'https://grupoboticario--uat.sandbox.my.salesforce-scrt.com'
                        }
                    );
                } catch (err) {
                    console.error('Error loading Embedded Messaging: ', err);
                }
            };
        </script>
        <script type='text/javascript' src='https://grupoboticario--uat.sandbox.my.site.com/ESWCRCMiawQDB1684273993056/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
    </body>
</html>
