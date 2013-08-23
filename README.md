A Riak Browser and Editor in Client Side Code
=================

# why

Riak's queries and other operations are URLs, and it returns results via http... so writing web apps with no middleware is a snap.  Having a query interface that sits in a value in the databse is satisfyingly self-referntial.

# how does it work

It uses javascript to query the database and provide a user interface to viewing, querying and editing values.

# installing

cURL it into your instance, then visit the key you just populated.

If you have the repo locally:
curl -X PUT -H "Content-Type: text/html" --data-binary "@this_file.html" "http://crawlbot:8098/riak/yourBucket/nameWhatYouWant.html"

If you want to pull from github:
curl -X GET "https://raw.github.com/facetcounter/RiakBrowserClient/master/edit.html" | curl -X PUT -H "Content-Type: text/html" --data-binary @- "http://crawlbot:8098/riak/yourBucket/nameWhatYouWant.html";

# feature set

## done
 * get value and put in edit field
 * put text in edit field into value
 * rudimentary mime type handling
 

## to do