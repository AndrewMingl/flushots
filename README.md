We were so impressed by the work that @tkompare did on his [Chicago Flu Shots](https://github.com/tkompare/flushots2013) web application for the 2013 flu season, that we decided to fork and improve upon it for the 2014 season. Our version has one big change - instead of being based on [Google Fusion Tables](https://tables.google.com/), it's instead powered by a [Socrata Open Data API](http://dev.socrata.com).

## About the Flu Shot Finder

![Flu Shot Finder](screenshot.png)

Given data about the location and hours of flu shot providers in your area, this application will help you locate the nearest place you can get the flu vaccine. It will even use geolocation in your browser to help find the nearest provider to your current location.

## Modifying 

1. [Fork the repo on Github](https://github.com/socrata/flushots/fork) so that you have your own copy to work with.
2. Locate data about the location of flu shot providers in your area. Hopefully, your local or state government has already provided this data, but if not, you can learn more about data hosting below.
3. If your data is already compliant with the schema below, you'll be able to use the app mostly without modifications. However, you'll still need to modify a few things:
  1. You'll need to change `sodaUrl` in `js/main.js:91` to the [API Endpoint](http://dev.socrata.com/docs/endpoints.html) for your dataset.
  2. Modify the branding in the `.modal-cdph` div in `index.html` to reflect your own instance of the app.
  3. Replace the [Google Maps API](https://developers.google.com/maps/) key in `index.html` with your own key.
  4. Update the city in `js/main.js`
4. If your data isn't compliant with the schema below, you can remap your data schema in `js/main.js`

## Deploying

## Data Schema

- `facility_name` - The name of the facility providing the vaccinations
- `begin_date` -
- `begin_time` -
- `contact` -
- `cost` -
- `end_date` -
- `end_time` -
- `hours` -
- `id` -
- `latitude` -
- `longitude` -
- `notes` -
- `phone` -
- `recurrence_days` -
- `url` -
- `street1` -
- `street2` -
- `city` -
- `state` -
- `postal_code` -

## Data Hosting

If vaccine provider data is not provided by your local government on Socrata, do not despair! There are other options available as well.

- If you're a local community group, free hosting is available via the [Socrata Community Data Platform](https://communities.socrata.com/). Your organization can [sign up](http://hackathon-in-a-box.org/open-data-apis/community-groups.html) and be granted an account that'll allow you to upload your data to Socrata and self-host your own API.
- If you're a [Code for America Brigade](http://www.codeforamerica.org/brigade/), you can also [sign up for free hosting](https://brigades.opendatanetwork.com/learn-more) on the [Brigade Open Data Sharing Platform](https://brigades.opendatanetwork.com/).

## Contributing

We warmly welcome [pull requests](https://help.github.com/articles/using-pull-requests/), so if there are modifications or improvements you'd like to make, feel free to fork this repo and send them our way! Please note that we may modify your pull requests to make sure they work properly with the main fork of the app.

## Warranty

This is sample code provided by [Socrata](http://www.socrata.com). No warranties or guaranties of any kind are granted. The code is licensed under the [MIT License](LICENSE.TXT), so have at it!