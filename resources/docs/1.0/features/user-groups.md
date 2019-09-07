# User Groups

This is the most awaited feature of AddChat. AddChat automatically detect your website user groups. And then as a website Admin, you can visit AddChat admin panel and set permissions for the groups. Like, which group can chat with which.


- [Setup User Groups](#Setup-User-Groups)
- [Set Groups Permissions](#Set-Groups-Permissions)
- [Groups List](#Groups-List)


<a name="Setup-User-Groups"></a>
## Setup User Groups

User groups option is by default `disabled`. You've to `enable` it from `Admin Panel -> Settings`. AddChat auto detects your website user groups. So your website must have user groups functionality.

<br>

To enable user groups option, your website should meet the following **requirements**.

1. `Groups` table
2. **Pivot** table for `Users` & `Groups` table, which contains sets of `User Id` and `Group Id`.

---

>{primary} We've designed the Group system according to most common and standard User Groups functionality.

---

Once you complete the above requirements, you can `enable` Groups option with the below steps

1. Open `Admin Panel` and click on `Settings`
2. Scroll down to **User Groups Table** section.
3. Click on `Group on/off` checkbox to turn `on` Groups functionality.
4. Fill in the following form fields

<br>

**Groups Table**

|Setting Name|Type|Description|
|:-|:-|
|Groups Table|`string`|enter your Groups table name e.g groups|
|Group Id|`string`|enter Group's table Id column name e.g id|
|Group Name|`string`|Group's table group name column e.g group_name|

<br>

**Users & Groups Pivot Table**

|Setting Name|Type|Description|
|:-|:-|
|Users & Groups Pivot Table Name|`string`|enter name of your users & groups pivot table e.g users_groups|
|Pivot table User Id|`string`|enter Pivot table User Id column name e.g user_id|
|Pivot table Group Id|`string`|enter Pivot table Group Id column name e.g group_id|


---

> {danger} All the above form fields are required in order to enable Groups functionality.

---

> {success} After completing all the above steps, click on &nbsp;<larecipe-button type="white" size="sm" radius="full">Save Settings</larecipe-button> and logout and login again.

---



<a name="Set-Groups-Permissions"></a>
## Set Groups Permissions

Once after you setup Groups configuration successfully, you'll see all your website `Groups` are fetched automatically in the `Admin Panel -> Chat Groups`. Here you can set **permissions** that which groups can chat with which group. 

<br>
So finally follow the below baby steps. 

1. On the `Admin Panel`, go to `Chat Groups`
2. Click on &nbsp;<larecipe-button type="primary" size="sm" rounded>Permissions</larecipe-button> on any Group, e.g Members
3. A Popup will open, simply check the checkbox with which groups, the e.g Members group can chat.
4. Click on &nbsp;<larecipe-button type="primary" size="sm" radius="full">Save Permissions</larecipe-button>


---

>{primary} Admin Group users can chat with everyone (all groups), basically there's no restrictions for the Admin Groups Users.

---

>{success} Once you set the Groups permissions the changes will take effect for all the users of your website.

---


<a name="Setup-User-Groups"></a>
## Setup User Groups

Once everything is done, then on the AddChat widget window, when the users click on `User Groups` tab, they can see all the `Groups` according to the `Groups Permissions`. 

<br>

And also when the users click on each `Group`, they can see all the `Users` in the `Group` and can chat with them.


>{info} This is also useful when a new user join your website and want to chat with any other user.