Deroù is a free collection of shell scripts for rapid deployment of Nginx/PHP/MariaDB, based on the popular [TuxLite](https://github.com/Mins/TuxLite).


The following are installed:-

-   Nginx
-   MariaDB
-   PHP-FPM + commonly used PHP modules
-   Postfix mail server (securely configured to be outgoing only)
-   Varnish cache (optional)


### Quick Install (Git)

    # Install git and clone Deroù
    aptitude install git
    git clone https://github.com/jiceb/derou.git
    cd derou
    
    # Edit options to enter server IP, MySQL password etc.
    nano options.conf
    
    # Make all scripts executable.
    chmod 700 *.sh
    chmod 700 options.conf
    
    # Install LNMP stack.
    ./install.sh
    
    # Add a new Linux user and add domains to the user.
    adduser johndoe
    ./domain.sh add johndoe yourdomain.com
    ./domain.sh add johndoe subdomain.yourdomain.com
    
    # Install Adminer or phpMyAdmin
    ./setup.sh dbgui
    
    # Enable/disable public viewing of Adminer/phpMyAdmin
    ./domain.sh dbgui on
    ./domain.sh dbgui off

