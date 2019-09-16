---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-04"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen:.screen}
{:codeblock:.codeblock}
{:note: .note}

# Getting started with {{site.data.keyword.weather_short}}
{: #insights_weather_overview}

Use {{site.data.keyword.weatherfull}} to incorporate weather data from
The Weather Company (TWC) into your {{site.data.keyword.Bluemix}} applications.
{:shortdesc}

**Attention:** Currently, the {{site.data.keyword.weather_short}} service **may not** be purchased
or used in the following countries or regions: Åland Islands, Albania, Algeria, American Samoa, Andorra, Angola, Anguilla, Antarctica, Antigua and Barbuda, Armenia, Aruba, Azerbaijan, Bahamas, Bahrain, Bangladesh, Barbados, Belarus, Belize, Benin, Bermuda, Bhutan, Bonaire, Sint Eustatius and Saba, Bosnia and Herzegowina, Botswana, Bouvet Island, British Indian Ocean Territory, Brunei Darussalam, Burkina Faso, Burundi, Cambodia, Cameroon, Cape Verde, Cayman Islands, Central African Republic, Chad, Christmas Island, Cocos (Keeling) Islands, Comoros, The Democratic Republic of the Congo, Cook Islands, Cote D'ivoire, Cuba, Curaçao, Djibouti, Dominica, Egypt, Equatorial Guinea, Eritrea, Ethiopia, Falkland Islands (Malvinas), Faroe Islands, Fiji, France, Metropolitan, French Guiana, French Polynesia, French Southern Territories, Gabon, Gambia, Georgia, Ghana, Gibraltar, Greenland, Grenada, Guadeloupe, Guam, Guernsey, Guinea, Guinea-Bissau, Guyana, Haiti, Heard And Mc Donald Islands, Iran (Islamic Republic of Iran), Iraq, Isle Of Man, Jamaica, Jersey, Jordan, Kazakhstan, Kenya, Kiribati, Korea, Democratic People's Republic of Korea, Kyrgyzstan, Lao People's Democratic Republic, Lebanon, Lesotho, Liberia, Libyan Arab Jamahiriya, Liechtenstein, Macau, Macedonia, The Former Yugoslav Republic of, Madagascar, Malawi, Maldives, Mali, Malta, Marshall Islands, Martinique, Mauritania, Mauritius, Mayotte, Micronesia, Federated States of, Moldova, Republic Of, Monaco, Mongolia, Montserrat, Mozambique, Myanmar, Namibia, Nauru, Nepal, Netherlands Antilles, New Caledonia, Niger, Niue, Norfolk Island, Northern Mariana Islands, Oman, Palau, Palestinian Territory, Occupied, Papua New Guinea, Paraguay, Pitcairn, Puerto Rico, Qatar, Reunion, Romania, Russian Federation, Rwanda, Saint Barthélemy, Saint Kitts and Nevis, Saint Lucia, Saint Martin (French Part), Saint Vincent and the Grenadines, Samoa, San Marino, Sao Tome And Principe, Saudi Arabia, Senegal, Serbia And Montenegro, Seychelles, Sierra Leone, Sint Maarten (Dutch Part), Solomon Islands, Somalia, South Georgia and The South Sandwich Islands, South Sudan, Sri Lanka, St. Helena, St. Pierre and Miquelon, Sudan, Suriname, Svalbard and Jan Mayen Islands, Swaziland, Syrian Arab Republic, Tajikistan, Tanzania, United Republic of, Timor-Leste, Tokelau, Tonga, Trinidad And Tobago, Tunisia, Turkmenistan, Turks and Caicos Islands, Tuvalu, Uganda, Ukraine, United Arab Emirates, United States Minor Outlying Islands, Uruguay, Uzbekistan, Vanuatu, Vatican City State (Holy See), Venezuela, Vietnam, Virgin Islands (British), Virgin Islands (U.S.), Wallis And Futuna Islands, Western Sahara, Yemen, Yugoslavia, Zaire, Zambia, Zimbabwe. This list is updated when additional information is available.

If you have an existing application that uses the
[Insights for Weather service](https://{DomainName}/docs/services/InsightsWeather/index.html){: new_window},
your app will continue to work without any modifications for 90 days after the introduction of
{{site.data.keyword.weather_short}}. To take advantage of the newly added APIs
and the improved pricing model, you can migrate your application to the new service.

Before you begin, create a {{site.data.keyword.Bluemix_notm}} web app in the dashboard
with a runtime such as Liberty for Java. Wait for your app to provision,
and then add the {{site.data.keyword.weather_short}} service to your app.

When you bind your app to {{site.data.keyword.weather_short}}, you are provisioning a
service instance with unique credentials. Your app uses these credentials with
the [REST APIs](https://twcservice.mybluemix.net/rest-api/){:new_window} to retrieve weather data.

Follow these steps to retrieve the service credentials from `VCAP_SERVICES`
and integrate the service instance with your app.

1. Navigate to your application overview page.
2. Go to the **Environment Variables** section. The `VCAP_SERVICES` information for each of your services is displayed.
3. Note the user name and password values from the {{site.data.keyword.weather_short}} service.
To try the [REST APIs](https://twcservice.mybluemix.net/rest-api/){:new_window},
you must enter these credentials when you are prompted to log in.
Your `VCAP_SERVICES` looks similar to the following example:

```
{
{
   "weatherinsights": [
      {
         "name": "Weather Company Data for IBM Bluemix",
         "label": "weatherinsights",
         "plan": "Free",
         "credentials": {
            "username": "d40845df-8125-441f-8e7c-e650726ce721",
            "password": "tDV0HGZz3O",
            "host": "twcservice.mybluemix.net",
            "port": 443,
            "url": "https://d40845df-8125-441f-8e7c-e650726ce721:tDV0HGZz3O@twcservice.mybluemix.net"
         }
      }
   ]
}
```

Each region is independent. You cannot use service credentials that are provisioned to you in one region to authenticate to a service in another region. Failure to enter proper credentials results in an *Unauthorized* message in the response body.
{:note}

# rellinks
{: #rellinks}
## samples
{: #samples}
* [{{site.data.keyword.weather_short}} demo app](http://weather-company-data-demo.mybluemix.net){: new_window}
* [{{site.data.keyword.weather_short}} Deep Dive video](https://youtu.be/pZHXIibziUo){: new_window}
* [Places Insights hands-on lab](https://github.com/IBM-Bluemix/places-insights-lab){: new_window}
* [{{site.data.keyword.Bluemix_notm}} + Weather sample app](https://github.com/IBM-Bluemix/insights-weather){: new_window}
* [IBM Cloud - Bare Metal, NYC Taxi Data, and Insights for Weather (YouTube tutorial)](https://www.youtube.com/watch?v=Uwmzpx9DZ5c){: new_window}

## api
{: #api}
* [REST API](https://twcservice.mybluemix.net/rest-api/){: new_window}

## compatible runtimes
{: #buildpacks}
* [Liberty for Java](https://{DomainName}/docs/runtimes/liberty/index.html){: new_window}
* [Node.js](https://{DomainName}/docs/runtimes/nodejs/index.html){: new_window}
* [Ruby](https://{DomainName}/docs/runtimes/ruby/index.html){: new_window}
* [Go](https://{DomainName}/docs/runtimes/go/index.html){: new_window}
* [PHP](https://{DomainName}/docs/runtimes/php/index.html){: new_window}
* [Python](https://{DomainName}/docs/runtimes/python/index.html){: new_window}

## general
{: #general}
* [Adding a service to your application](https://{DomainName}/docs/services/reqnsi.html){: new_window}
* [End-to-end development](https://{DomainName}/docs/cfapps/ee.html){: new_window}
* [{{site.data.keyword.Bluemix_notm}} Pricing Sheet](https://{DomainName}/pricing/){: new_window}
* [{{site.data.keyword.Bluemix_notm}} Prerequisites](https://developer.ibm.com/bluemix/support/#prereqs){: new_window}
