# Realtime Notifications

This is the most advanced feature of AddChat. We've implemented **Pusher** & developed a new **Internal** notification system for realtime and chatting. 

<br>

**Internal** notification system is a very light weight and high performance realtime chatting notification system built using VueJs, which do not require any additional server setup. It works smoothly behind the scenes.

<br>

Internal notification system sends regular `Asynchronous HTTP/S Requests` to the server for getting latest messages updates. For the geeks who already know what it means, let us tell you a secret. It only runs a **Single `SELECT`** database query in a **Single `Table`** to fetch latest messages updates. So it never lower your server performance.

<br>

Also the **total no. of `records`** fetched from the **Single `SELECT`** database query are equal to the **total no. of users chatting at the same time**. Using this, you can calculate the server load of the **Internal** notification system.

---

>{primary} You can easily switch between **Pusher** & **Internal** notification system with just one click.

---

>{warning} When you switch between Pusher & Internal notifications, it takes effects after logout and login again, for the users who are already logged in.


- [Internal Notifications](#Internal-Notifications)
- [Pusher Notifications](#Pusher-Notifications)
- [Pusher Setup](#Pusher-Setup)


<a name="Internal-Notifications"></a>
## Internal Notifications

Internal notification system fetches the following things in realtime (without refreshing the page)

1. Total received messages of a contact (user)
2. New messages while chatting with a user
3. Message is seen or not

---


<a name="Pusher-Notifications"></a>
## Pusher Notifications

Pusher notification system fetches the following things in realtime.

1. Total received messages of a contact (user)
2. New messages while chatting with a user
3. Message is seen or not
4. User is typing...


---


>{success} If you're a running a small business website, where you need a realtime chat support and user to user chat function, you can use the **Internal** notification system on the live website without any hesitation. 

---

>{primary} **Internal** notification system saves your **Pusher** monthly subscription fees.

---


<a name="Pusher-Setup"></a>
## Add Pusher API Credentials

By default, the **Internal** notification system is `enabled` when you first setup AddChat on your website. So if you want to switch to `Pusher` notifications, then you need to [Signup on Pusher](https://pusher.com/signup) and `create an app` and get the Pusher API credentials.

<br>

Once you get the API credentials, come back to your website, open AddChat widget and -

1. Go to `Admin Panel -> Settings` and scroll down to **Realtime Notifications** section.
2. Select `Notification Type` to `Pusher Notification``
3. Then enter the fields-
    - Pusher App Id
    - Pusher Key
    - Pusher Secret
    - Pusher Cluster
4. Click on save settings and you're done.


>{info} After switching to `Pusher Notifications` logout and login again to see the effects.

