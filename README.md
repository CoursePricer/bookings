# Bookings

You can link your CoursePricer installation to a booking form on your own website by following the installation steps below. Some example forms are included in the 'examples' folder but you are free to use any form you wish.

### Implementing the form on your website
+ For now, make a new page on your website that includes the example code from one of the 'examples' inside this repository.
+ Go to API Access (https://www.coursepricer.com/admin/api-access/) and Generate a new API Token by clicking on the button.
+ Update the form `action` value to the endpoint that your form should submit to.
+ Update the JavaScript code by replacing the 'API TOKEN GOES HERE' string with your API Token.
+ Upload your form and take note of the URL that it resides at e.g. https://www.yourschool.com/form.html

### Linking the form to CoursePricer
To show the booking button on the CoursePricer Quotation page follow the steps below:
+ Inside CoursePricer admin, navigate to the booking tab inside School Settings (https://www.coursepricer.com/admin/settings/) and then:
	+ enter the URL that your new booking form is at.
	+ enter the text you'd like to show on the button on CoursePricer Quotation pages.
+ Hit Save.

Your form will now be linked and a new button will appear when students make quotations through CoursePricer. When they click on that button they'll be redirected to the URL that you provided. The quotation will be retrieved and displayed on your page above the form in our examples. Our examples use JavaScript for simplicity but developers will also be able to make this work using other languages if desired.

To remove the booking button from your installation, remove the URL from settings.

### Security
+ API requests must originate from the domain of the URL that has been specified in settings.
+ Quotations can only be retrieved for the school id(s) that the API Key is linked to.
+ Quotations can only be retrieved for 10 minutes after the booking was created.

If you are worried about other people using your API Key then we recommend you hit the API using a server-side language such as PHP instead.

