#cP Starter Style - Light

cP Starter is a base style intended for designers, developers, server admins, resellers, and/or anyone who isn’t afraid to code.  It is a professional, yet minimalistic approaches that can be used as is or adapted to match your company’s branding and logo. 

If you're looking for a DARK version, visit [cP Starter Dark](https://github.com/longster/cP-Starter-Dark).

> ###cP Starter is intended for you to modify the appearance of the cPanel interface and kickstart your own custom style. 


##Custom Style Installation##
You’ll want to identify the type of role that best suits your needs in order to complete the installation. In addition, cP Starter is only compatible to **cPanel & WHM 56 or later**. 

1. Download and uncompress the zip files

2. Upload (via FTP) all of the files and place them under “cP_Starter_Light” folder below the directory “styled” (Note: if the directory folders do not exist, create them in the right order): 

    - **Server**: 
        + `/var/cpanel/customizations/styled/cP_Starter_Light/`
        
    - **Reseller**: 
        + `var/cpanel/reseller/styled/cP_Starter_Light/`
        
    - **cPanel User**: 
        + `/home/username/var/cpanel/styled/cP_Starter_Light/` (Note: username - represents the cPanel account's username)

3. Generate custom icons via command line (Note: this is optional as it replaces existing icons): 

    - **Both Server & Reseller**:
        + Log in to the server via SSH as a root or reseller user
        + Run the command line: 
            - `/usr/local/cpanel/bin/sprite_generator --theme paper_lantern --style cP_Starter_Light`

4. Change your style interface:

    - **Server**:
        + Log in to the server via SSH as the root user
        + Run the command: 
            - `ln -s /var/cpanel/customizations/styled/cP_Starter_Light default_style` (Note: This sets the default for all new accounts. It does not modify any existing accounts. To do so, you will need to change default style under “cPanel User” instruction.)
            
    - **Reseller**: 
        + Login to cPanel
        + Navigate to Change Style: Home >> Preferences >> Change Style
        + Select “Set as Default” to apply every cPanel account or select “Apply” for specific account.
        
    - **cPanel User**:
        + Login to cPanel
        + Navigate to cPanel Style: Home >> Preferences >> Change Style
        + Click “Apply”

5. Change cPanel default logo to your own brand logo:

    - **Both Server and Reseller**:
        + Login to WHM
        + Navigate to Branding:  cPanel > Branding 
        + Upload your logo under Company Logo


If you see any incorrect information, please contact me or open an issue. Thanks!


###Resources###
- [Setting default style on the box and removing ability for user to change their styles](https://blog.cpanel.com/how-to-set-a-default-style-with-paper-lantern/)
- [cPanel Branding Basics: A Guide for Reseller Hosts](https://blog.cpanel.com/cpanel-branding-basics-a-guide-for-reseller-hosts/)
- [Create a Custom cPanel Style](https://documentation.cpanel.net/display/SDK/Tutorial+-+Create+a+Custom+cPanel+Style)




