# It is never too soon to be fitted for a tinfoil hat

@hirozed  
jimreevior.com

## Security in code

### Sanitize Input / Escape Output

 - Never trust the data
  - Even your own

```php
is_array();
is_string();
is_int();
filter_var();
  // used to confirm variable you're getting does what you expect
filter_input();
  // used to filter the global variables so you're not just using them raw
```

#### Escaping

This is on the output side

```php
esc_html();
esc_url();
esc_attr();
esc_js();
wp_kses_post();
  // used kind of as a catchall — used for content filter, you can define a whitelist
```

### Prevent SQL Injections

Always try to use the built in WordPress functions

 - WP_Query
 - wp_update_post();
 - wp_delete_post();
 - update_option();

If you *must* create a SQL query, take advantage of the `$wpdb` global

### Nonces

"Numbers used once" — numbers that can verify the user and time a field was modified.

Always include a nonce field when adding meta box fields. Prevents others from spoofing or taking over.

Used to validate in the admin.

## Security on Server

### Hosting Choices

  - WordPress Managed Hosting
    - Handles server Security
    - WP core updates
    - Tuned for WP
  - Shared Hosting
    - They keep server up to date
    - Wordpress security is up to you.
  - Roll your own
    - Maintenance & security are your responsibility
    - Not for the faint of heart.

#### Other suggestions

  - Move wp-config.php
  - Change permissions for core files
  - Turn off editing  
  Add to wp-config.php: `define( 'DISALLOW_FILE_EDIT', true );`  
  *Disallow editing of theme files, etc. from admin inteface*

## Security Plugins

  - Wordfence
  - iThemes Security
  - Jetpack -- use for security only if you're using other items in Jetpack.
  - Login Lockdown -- use along with Wordfence.
  - 2 Factor Authentication

## Resources
  - Mark Jaquith's WC Phoenix 2011 talk
  - Hardening WordPress
  - Plugin Security
  - Theme Security
  - Aluminum Foil Hats
