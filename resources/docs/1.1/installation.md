# Codeigniter Installation

AddChat CodeIgniter Pro comes with an installer that makes the installation process fully automated and smooth 🍻

---

![AddChat CodeIgniter Pro Installer](https://addchat-pro-docs.classiebit.com/images/addchat-codeigniter-pro-installer.jpg "AddChat CodeIgniter Pro Installer")

---

> {info.fa-youtube} A complete video tutorial guide for getting started quickly is **Coming Soon**

---

- [Server Requirements](#Server-Requirements)
- [Remember](#Remember)
- [Install](#Install)
- [Installer Instructions](#Installer-Instructions)


<a name="Server-Requirements"></a>
## Server Requirements

* PHP version **5.6** or newer is recommended.
* Make sure **.htaccess** is enabled.
* CodeIgniter website with an **Authentication** (user-login) system. 


<a name="Remember"></a>
## Remember

* The website directory must have proper **write** permissions e.g `sudo chown -R :www-data yourwebsite`
* Change CSRF regenerate to `FALSE` in `application/config/config.php` `$config['csrf_regenerate'] = false`


<a name="Install"></a>
## Install

1. Download & Unzip the package.
2. Copy the **addchat_installer_pro** folder and paste it into your website root directory.
3. After doing so, your website directory will look like this.

    ```bash

    yoursite.com
    │
    ├── addchat_installer_pro
    ├── application
    ├── system
    │
    ├── ..
    ├── ..
    ├── ..
    │
    ├── .htaccess
    └── index.php

    ```

4. Visit `yoursite.com/addchat_installer_pro` to run the installer. 


>{warning} Make sure **.htaccess** files exist and not hidden.

---

> {danger} Do not forget to delete the **addchat_installer_pro** folder after successful installation.

---

<a name="Installer-Instructions"></a>
## Installer Instructions

#### Database

- Enter your website's existing database credentials.

<br>

#### Assets

- Enter your website assets folder path.

<br>

#### Config

- Enter your website config folder path. e.g `application/config`
- Enter **LOGGED-IN USER-ID SESSION KEY NAME** e.g user_id

>{info} The $_SESSION variable key name in which your application stores the logged-in user id e.g $_SESSION['user_id'] then the key is **user_id**

<br>

#### Application

- Enter **Controllers** Folder Path e.g `application/controllers`
- Enter **Libraries** Folder Path e.g `application/libraries`
- Enter **English Language** Folder Path e.g `application/language/english`

<br>

#### License Code

- You'll need to enter the license code to complete the installation process.

>{info} Remember, one license code is valid for one domain only. Contact support for more details.

---

>{success} And finally click install to start the installation process.

---


### After successful installation, you need to do one simple step manually.

1. Open the common layout file, mostly the common layout file is the file which contains the HTML & BODY tags.

    - Copy AddChat CSS code and paste it right before closing **&lt;/head&gt;** tag

        ```php
        <!-- 1. Addchat css -->
        <link href="<?php echo base_url('addchat/css/addchat.min.css') ?>" rel="stylesheet">
        ```
    
    - Copy AddChat Widget code and paste it right after opening **&lt;body&gt;** tag

        ```php
        <!-- 2. AddChat widget -->
        <div id="addchat_app" 
            data-baseurl="<?php echo base_url() ?>"
            data-csrfname="<?php echo $this->security->get_csrf_token_name() ?>"
            data-csrftoken="<?php echo $this->security->get_csrf_hash() ?>"
        ></div>
        ```

    - Copy AddChat JS code and paste it right before closing **&lt;/body&gt;** tag

        ```php
        <!-- 3. AddChat JS -->
        <script src="<?php echo base_url('addchat/js/addchat.min.js') ?>"></script>
        ```

    <br>

    #### The final layout will look something like this

    ```php
    <head>

        <!-- **** your site other content **** -->

        <!-- 1. Addchat css -->
        <link href="<?php echo base_url('addchat/css/addchat.min.css') ?>" rel="stylesheet">

    </head>
    <body>

        <!-- 2. AddChat widget -->
        <div id="addchat_app" 
            data-baseurl="<?php echo base_url() ?>"
            data-csrfname="<?php echo $this->security->get_csrf_token_name() ?>"
            data-csrftoken="<?php echo $this->security->get_csrf_hash() ?>"
        ></div>


        
        <!-- **** your site other content **** -->



        <!-- 3. AddChat JS -->
        <script src="<?php echo base_url('assets/addchat/js/addchat.min.js') ?>"></script>
        
    </body>
    ```

---

>{success} Setup finishes here, now heads-up straight to **[Configurations](/{{route}}/{{version}}/configurations)** docs
