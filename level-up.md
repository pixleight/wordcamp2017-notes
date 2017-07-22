# Level Up! -- Taking your Wordpress Code up a Notch

Amanda Giles
https://amandagiles.com/wcbos17

## Debugging

Basic debugging:

```php
define( 'WP_DEBUG', true );
define( 'WP_DEBUG_LOG', true );
define( 'WP_DEBUG_DISPLAY', false );
```

Puts debugging in log, but doesn't display on screen

## Developer plugins

 - Developer plugin
 - Debug Bar plugin
 - Query Monitor plugin

## Hooks

An event or point-in-time within WP code that will allow additional code to be run

### Action hooks

Run code at a certain point within the code  
*Examples - initialization, before main query, header or footer, etc*

### Filter hooks

Allow you to alter information — passed information and then you can return it altered (or not!)

## Action hook example

```php
// Action hooks are triggered by do_action()
do_action('wp_logout');

// ...then hooked into with add_action()
add_action('wp_logout' 'my_wp_logout');
function my_wp_logout(){
  // code here
}
```

---

## Common hooks

 - init
 - template_redirect
 - wp_head
 - wp_enqueue_scripts
 - pre_get_posts - *modify main query before it's run*
 - the_content
 - wp_footer
 - save_post

**pre_get_posts**

Happens after $query object is created, but before that query is run

## WP_Query

WP_Query allows you to easily generate complex post queries

If you use the_post() with your query, you need to run wp_reset_postdata() after proessing your query results to reset query to the original query on that page.

## Shortcodes

Takes code from posts's TinyMCE editor to create code on frontend.

## Transient API

A mechanism by which Wordpress stored temporary data — more complex than retrieving a single database cell

## WP-CRON

WordPress' internal time-based scheduling system

Only triggered by site visits, but missed tasks are not lost — they'll be executed on the next site visit.
