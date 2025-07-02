
Food Truck owners install the Food Truck Nerdz Tracker app.

## Step 1
Sign up for business owner account, provide personal details.

## Step 2
Add a Blank Food Truck. Owner can add multiple blanks to their list. Owner then clicks on a Food Truck to begin setting it up.

## Step 3
Populate Food Truck Profile manually or through integrations. Tell owner they can import their profile from Facebook or Instagram and optionally have those profiles updated whenever they change their food truck details in the app. Connect socials. Pull profile details from Facebook or Instagram Page. If any data exists, compare the imported data to the existing data and check for inconsistencies, and ask the owner to decide what to keep.

Options:
- Manually
- Facebook import
	- Food Truck Name
	- Address
	- Service Area
	- Tagline
	- Description
	- Menu
	- Schedule
	- Profile Photo
	- Use AI to infer details from photos.
		- Food Category
		- Description (if missing)
		- Schedule
	- Check for conflicting information before committing details.
- Instagram import
	- Food Truck Name
	- Address
	- Profile Photo
	- Use AI to infer details from profile description:
		- Service Area
		- Tagline
		- Description
		- Schedule
		- Food Category
	- Use AI to infer details from photos:
		- Food Category


## After import
After the owner finishes, show them the profile, and offer to continuously sync their profile with their FB and Instagram Pages, using 2-way sync.


Offer to sync details for:
- Facebook Page:
	- All details
	- Profile Photo
- Instagram Page:
	- Food Truck Name
	- Website
- Square profile:
	- Menu
	- Business Name
- Clover profile:
	- Menu
	- Business Name


### Sync
If the owner changes any information on their socials, we sync the changes to our database, and then sync them to their other socials. Then, we notify the owner that their details have been updated.

Ideally we'd like them to make changes through our app instead.

If they update their Instagram description, we should not automatically update but instead ask the owner if they would like to review the update.

#### Implementation details

We will subscribe to changes by using Webhooks, if available. As a fallback, we will periodically sync the changes to us, and to their other social media. Webhooks are available for Facebook Pages and Instagram Business Pages.

##### Facebook API
>Does facebook's api allow app developers to subscribe to changes made on a page the app user connects to the app?

Yes, Facebook's API allows app developers to subscribe to changes made on a page that the app user connects to. This is facilitated through Webhooks, which can send real-time notifications of changes to your Pages. For example, you can receive updates whenever users post to your feed, comment on a post, or like your posts. To set this up, you need to configure the Webhooks product and install your app on the Facebook page. The app must have the necessary permissions and a Page access token to subscribe to these notifications[1](https://developers.facebook.com/docs/graph-api/reference/page/subscribed_apps/)[2](https://developers.facebook.com/docs/graph-api/webhooks/getting-started/webhooks-for-pages/).

##### Instagram API
> how about instagram

Instagram's API also allows developers to subscribe to certain changes related to Instagram accounts, particularly for Instagram Business or Creator Accounts. This is facilitated through Webhooks, which can send real-time notifications for specific events such as comments on media objects, mentions, or story insights. To set up these notifications, developers need to configure Webhooks in the App Dashboard, ensure the app has the necessary permissions, and enable Page subscriptions. The app must also complete App Review to receive certain webhook

#### Square
- Use the [Catalog API](https://developer.squareup.com/docs/catalog-api/what-it-does) . [Design a Catalog](https://developer.squareup.com/docs/catalog-api/design-a-catalog)




## Gotchas

### Multiple trucks to single social
(Many-to-One Mapping Issues)

Some food truck owners may have the same multiple food trucks using the same concept/brand, but only have one Facebook page or Instagram Page. When they link a social media, check the ID to see if it's been used already. Food truck owners will still be able to import profile information to multiple Food Trucks from the same social media pages, but we cannot sync multiple trucks' details to the social media.

Let the user know our service can track both food trucks but can only sync profile information for one truck. They will have to select a "primary" truck for the sync. They can still post updates to social media from either truck, with location information embedded in the post.

The only consequences are that the food truck's social media profiles will not have all information. Users will still be notified when a food truck comes to them.
