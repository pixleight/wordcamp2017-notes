# Building an App with Wordpress' REST API
### Greg Opperman

 - http://gopperman.github.io/wordcamp2017
 - @gopperman

---

## REST API Basics

**Use REST API if...**
 - you need a rich, interactive experience
 - you'd like to release an app on multiple platforms

**Examples**
 - Wordpress.com: Calypso
 - NYT to power live blogs w/ React, Backbone.js
 -

**Typical request:**  
`/wp-json/wp-json/v2/posts?search=dance`  
returns JSON

Adding data to JSON:
```php
// functions.php
function my_rest_prepare_post( $data, $post, $request ) {
  $_data = $data->data;
  $_data['URL'] = get_post_meta( $post->ID, 'URL', true);
  $data->data = $_data;
  return $data
}
add_filter( 'my_rest_prepare_post', 'prepare_post', 10, 3 );
```

## React

**Typical request:**

```javascript
const requestUrl = 'url';
retch(requestUrl).then((response) => {
    return response.json()
  })
  .then((data) => {
    this.setState({
      response: data,
      })
    })
  .catch((err) => {
      // Error
    })
```

Encourages unidirectional data flow with flux/redux

## Tools and Frameworks

 - create-react-app
 - react-native
 - wp-react-skeleton
 - Picard
 - wp-api-react

### Learning Resources

 - Intro to React
 - WP REST API v2 Guide
 - WP REST API Developer Reference 
