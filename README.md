# odin-links-and-images

## use of rel attribute in anchor element in html

You may have noticed that we snuck in the rel attribute above. This attribute is used to describe the relation between the current page and the linked document.


The noopener value prevents the opened link from gaining access to the webpage from which it was opened.

The noreferrer value prevents the opened link from knowing which webpage or resource has a link (or ‘reference’) to it. The ##noreferrer value also includes the noopener behaviour and thus can be used by itself as well.

Why do we need this added behaviour for opening links in new tabs?

Security reasons. The prevention of access that is caused by ##noopener prevents phishing attacks where the opened link may change the original webpage to a different one to trick users. This is ##referred to as tabnabbing. Adding the noreferrer value can be done if you wish to not let the opened link know that your webpage ##links to it.

Note that you may be fine if you forget to add rel="noopener noreferrer" since more recent versions of browsers provide security if only target="_blank" is present. Nevertheless, in line with good coding practices and to err on the side of caution, it is recommended to always pair a target="_blank" with a rel="noopener noreferrer".


## Absolute and Relative link

Absolute and relative links are a tricky concept to build a good mental model of, a metaphor may help:

Think of your domain name (town.com) as a town, the directory in which your website is located (/museum) as a museum, and each page on your website as a room in the museum (/museum/movie_room.html and /museum/shops/coffee_shop.html). Relative links like ./shops/coffee_shop.html are directions from the current room (the museum movie room /museum/movie_room.html) to another room (the museum shop). Absolute links, on the other hand, are full directions including the protocol (https), domain name (town.com) and the path from that domain name (/museum/shops/coffee_shop.html): https://town.com/museum/shops/coffee_shop.html.
