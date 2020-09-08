# API Documentation for OnlineApps

All requests relative to https://requests.onlineapps.cloud/api

- Post request body is usually `application/x-www-formurlencoded`
- Auth token is passed as `Authorization: "Bearer {{token}}"` header, see [Confidential/login.md](Confidential/Login/login.md) to get token
- When `{{}}` is used, it is a placeholder (Most often for uid/token)

## Table of contents
- Cofidential
  - App
    - [List linked apps](Confidential/App/list_linked_apps.md)
    - [List linked apps for RDP](Confidential/App/rdp_apps.md)
    - [Link app](Confidential/App/link_app.md)
    - [Unlink app](Confidential/App/unlink_app.md)
    - [List associations](Confidential/App/list_associations.md)
    - [Set associations](Confidential/App/set_associations.md) 
  - Login
    - [Login](Confidential/Login/login.md)
    - [Logout](Confidential/Login/logout.md)
    - [Sign up](Confidential/Login/signup.md)
  - Settings
    - OTP
      - [Generate new OTP secret](Confidential/Settings/OTP/generate_new_otp.md)
      - [Get OTP setup link](Confidential/Settings/OTP/get_otp_link.md)
      - [Get OTP status](Confidential/Settings/OTP/get_otp_status.md)
      - [Set OTP status](Confidential/Settings/OTP/set_otp_status.md)
    - [Update bindings](Confidential/Settings/update_bindings.md)
    - [Edit account](Confidential/Settings/update_account.md)
    - [Delete account](Confidential/Settings/delete_account.md)
    - [Set avatar](Confidential/Settings/set_avatar.md)
    - [Delete avatar](Confidential/Settings/delete_avatar.md)
  - Server
    - [Get created apps](Confidential/Server/get_created_apps.md)
    - [Create app](Confidential/Server/create_app.md)
    - [(WIP) Edit app]()
    - [Delete app](Confidential/Server/delete_app.md)
    - [Get created Servers](Confidential/Server/get_created_servers.md)
    - [Create server](Confidential/Server/create_server.md)
    - [Delete server](Confidential/Server/delete_server.md)
    - [(WIP) Get heartbeat]()
  - Utils
    - [Get menu XML](Confidential/Utils/xml_menu.md)
    - [Get db XML](Confidential/Utils/xml_db.md)
    - [Get credit](Confidential/Utils/get_credit.md)
    - [Get icon list](Confidential/Utils/icon_list.md)
    - [Get login history](Confidential/Utils/login_history.md)
- Public
  - Apps
    - [Get all apps](Public/Apps/list_all_apps.md)
    - [Get all apps by category](Public/Apps/list_apps_in_all_categories.md)
    - [Get apps in a category](Public/Apps/list_apps_in_category.md)
    - [Search apps](Public/Apps/search.md)
    - [Get all categories](Public/Apps/list_categories.md)
    - [Get subcategories of a category](Public/Apps/list_subcategories.md)
  - User
    - [Does user exist](Public/User/existing_user.md)
    - [Get user's avatar](Public/User/get_avatar.md)