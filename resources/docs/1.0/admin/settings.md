# Settings

Here you can manage AddChat widget global settings.

> {warning} Please, carefully read all the guidelines provided below for each setting, or else it may break down the your site.

---

> {danger} Please make sure you use the exact same setting value type e.g string, numeric, etc.


- [General](#General)
- [Widget Config](#Widget-Config)
- [Users Table](#Users-Table)
- [User Groups Table](#User-Groups-Table)
- [Guest Mode](#Guest-Mode)

--- 

<a name="General"></a>
## General Settings

These are your website specific settings.


|Setting Name|Type|Description|
|:-|:-|
|Site Name|`alpha-numeric`|Brand/Website name|
|Site Logo|`image:jpg|jpeg|png`|You'll see this logo on the AddChat widget and admin panel|
|Chat Icon|`image:jpg|jpeg|png`|You'll see this logo as the widget icon|
|Footer Text|`alpha-numeric`|Change the footer text according to your Brand|



<a name="Widget-Config"></a>
## Widget Config

These are the chat widget main configs


|Setting Name|Type|Description|
|:-|:-|
|Admin User Id|`integer`|Enter the Admin Id value from the users table (only this user will see the admin panel)|
|Pagination Limit|`integer`|Enter the total records value that are fetched in single time (be careful, greater the value, greater the database load)|
|Upload Path|`integer`|Enter the path, where to upload the profile pic and message attachments|
|Assets Path|`integer`|Enter the AddChat assets path, from where AddChat will pick up the fonts, placeholder image and notification sound|

---

>{danger} Please be sure to keep the `Upload Path` writable, or else it'll through error while uploading images



<a name="Users-Table"></a>
## Users Table

Enter your website `users` table name and columns name, so that AddChat can use your existing users base.

>{success} AddChat never modify any data in your `users` table and never read the `password` or any other sensitive column except `user id` and `email`


|Setting Name|Type|Description|
|:-|:-|
|Users table name|`string`|Enter the Users table name|
|User Id|`string`|Enter the user id column name in the users table|
|User Email|`string`|Enter the user email column name in the users table|

---



<a name="User-Groups-Table"></a>
## User Groups Table

>{warning} Please read `Features -> User Groups` section for more info about `Groups` Function

Enter `groups` table name and columns name, so that AddChat can fetch & use your existing user groups.

>{success} Again, AddChat never modify any data the `groups` table and never assign any `group` to any `user`


|Setting Name|Type|Description|
|:-|:-|
|Groups|`bool`|Check/Uncheck the checkbox to enable/disable groups function|
|Groups Table Name|`string`|Enter the groups table name|
|Group Id|`string`|Enter the groups table's Group Id column name|
|Group Name|`string`|Enter the groups table's Group Name column name|
|Users & Groups Pivot Table Name|`string`|enter name of your users & groups pivot table e.g users_groups|
|Pivot table User Id|`string`|enter Pivot table User Id column name e.g user_id|
|Pivot table Group Id|`string`|enter Pivot table Group Id column name e.g group_id|

---



<a name="Guest-Mode"></a>
## Guest Mode

>{warning} Please read `Features -> Customer Support` section for more info about `Guest Mode` Function

Enter `Guest/Support Group` id (value), the group who chats with the `Guests` (the users who are not registered or logged in into the your website)


|Setting Name|Type|Description|
|:-|:-|
|Guest Mode|`bool`|Check/Uncheck the checkbox to enable/disable Guest Mode function|
|Guest Group Id|`integer`|Enter the Guest/Support Group id (value)|


---



