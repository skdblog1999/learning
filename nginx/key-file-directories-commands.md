# Nginx Key Files, Commands & Directories

## /etc/nginx

Contains all the configurations of nginx

## /etc/nginx/nginx.conf

Default configuration entry point used by nginx service. The configuration file sets up global settings.

## /etc/nginx/conf.d

Contains the default HTTP server configuration file.

Files in this directory ending in .conf are included in top-level http block from within the /etc/nginx/nginx.conf .

## /var/log/nginx

Default log location for NGINX.

contains access.log & error.log

access.log  contains an entry of each request NGINX serves.

error.log contains error events and debug information if the debug module is enabled.



# Nginx Commands

## nginx -h

shows the nginx help menu

## nginx -v

shows the nginx version

## nginx -V

shows the nginx version, build information, and configuration  arguments, which shows the modules built into the nginx binary

## nginx -t

tests the nginx configuration

## nginx -T

Tests the nginx configuration and prints the validated configuration to the screen. This command is useful when seeking support.

## nginx -s signal

The -s signal sends a signal to the nginx master process. You can send signal such as stop, quit, reload and reopen. 

The stop signal discontinues the nginx process immediately.

The quit signal stops the NGINX process after it finishes processing inflight requests.

The reload signal reloads the configuration

The reopen signal instructs NGINX to reopen log files. 

