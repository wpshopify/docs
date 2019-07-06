# Requirements

WordPress powers over [30% of all websites and over 60%](https://w3techs.com/technologies/details/cm-wordpress/all/all) of all CMS platforms today.

Because so many people rely on WordPress, the core developers must take a fairly conservative approach when deciding which versions of PHP to support. While understandable, one of the drawbacks is leaving millions of sites running legacy versions of PHP thereby creating massive security vulnerabilities—both for site owners and its users.

We believe that one of the best ways to make WordPress more secure is by requiring users to upgrade their systems as a prerequisite to using our plugins. With this in mind, the minimum requirements for WP Shopify are:

## Minimum Requirements

-  PHP 5.6 or greater
-  WordPress 4.7 or greater
-  PHP `memory_limit` of 64 MB <small>(256 MB if running into syncing timeout issues)</small>
-  PHP `max_execution_time` of 100 <small>(300 if running into syncing timeout issues)</small>
-  Valid HTTPS certificate
