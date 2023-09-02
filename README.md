<div id="paypal-button-container-P-8UK99422S8253240BMTZUB6Q"></div>
<script src="https://www.paypal.com/sdk/js?client-id=sb&vault=true&intent=subscription" data-sdk-integration-source="button-factory"></script>
<script>
  paypal.Buttons({
      style: {
          shape: 'rect',
          color: 'blue',
          layout: 'vertical',
          label: 'subscribe'
      },
      createSubscription: function(data, actions) {
        return actions.subscription.create({
          /* Creates the subscription */
          plan_id: 'P-8UK99422S8253240BMTZUB6Q'
        });
      },
      onApprove: function(data, actions) {
        alert(data.subscriptionID); // You can add optional success message for the subscriber here
      }
  }).render('#paypal-button-container-P-8UK99422S8253240BMTZUB6Q'); // Renders the PayPal button
</script>
