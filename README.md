```javascript
javascript:(function(a){window.trelloAppKey="optional";window.trelloIdList="optional";var b=a.createElement("script");b.src="https://raw.github.com/Asgaroth/Trello-Bookmarklet/master/trello_bookmarklet.js";a.getElementsByTagName("head")[0].appendChild(b)})(document);
```

This is a <a href="http://en.wikipedia.org/wiki/Bookmarklet">bookmarklet</a> you can use to create a card in <a href="https://trello.com">Trello</a> from Redmine

The first time you run it on a site, it will walk you through a simple setup:

 1. Input your API Key (which you can get at https://trello.com/1/appKey/generate)
 2. Authorize the site to interact with Trello
 3. Select the list that you'd like the bookmarklet to add cards too

The card created in Trello will 

- attempt to use the name of the Redmine issue
- include a link to the case in the card description
- add the corresponding labels: red for redbug, green for user stories, etc...
- (optionally) include any selected text in the description

If you'd rather not add your appKey and idList for every new domain, you can modify the bookmarklet and include values for `window.trelloAppKey` and `window.trelloIdList` (currently both have the value `"optional"`)

**Note:** This basic concept originated with https://github.com/markdrago/cardorizer; this approach doesn't require you to run a server
