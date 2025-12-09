<html>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

      window.addEventListener( "onEmbeddedMessagingReady", () => {  
				console.log("Inside onEmbeddedMessagingReady");
	            embeddedservice_bootstrap.utilAPI.setSessionContext([
	                {
	                    "name": "_AgentContext",
	                    "value": {
	                        "valueType": "StructuredValue",
	                        "value": {
	                            currentPage:"https://infallibletechie.github.io"
	                        }
	                    }
	                }
	            ])
	            .then(() => {
	                console.log("Successfully set the agent context!!!");
	            })
	            .catch((error) => {
	                console.log("Error thrown while setting agent context." + error);
	            });
			} );

			embeddedservice_bootstrap.init(
				'00DHo00000AJRqg',
				'MIAW',
				'https://infallibletechieblog.my.site.com/ESWMIAW1752090006821',
				{
					scrt2URL: 'https://infallibletechieblog.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://infallibletechieblog.my.site.com/ESWMIAW1752090006821/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</html>
