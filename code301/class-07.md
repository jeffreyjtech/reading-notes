# Read 07 - REST

## [How I explained REST to my brother](https://gist.github.com/brookr/5977550)

1. Who is Roy Fielding?
    - He participated in writing the first web servers which sent information across the internet. He also did research into how the web should be structured.
    ***
2. Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?
    - Because the technologies crafted for small, closed systems ended up having incompatible ways of communicating with each other. Like how people speaking different languages can't understand each other, the ad-hoc solutions to networking that came after Roy Fielding's work used different vocabulary and grammar, and they could not work with each other.
    ***
3. What is the HTTP protocol that Fielding and his friends created?
    - HTTP is about applying verbs to nouns in the web space using a universal set of nouns and verbs. Thus, all machines would be able to talk to one another. An example of the benefit of HTTP is that a request which may not have met its intended resource can be redirected to the right place instead of being rejected outright.
    ***
4. What does a `GET` do?
    - `GET` retrieves information from a web resource for processing or representation.
    ***
5. What does a `POST` do?
    - `POST` creates a new resource altogether on another system
    ***
6. What does `PUT` do?
    - `PUT` replaces the representation of a existing resource with new data.
    ***
7. What does `PATCH` do?
    - `PATCH` is a request which partially updates or partially changes an existing resource
    ***

## API Keys

Did I get API keys for the following APIs?

1. **Geocoding API** - Yes
2. **Weather Bit API** - Yes
3. **Yelp API** - No (only required for stretch goal)
4. **MovieDB API** - Yes

## Things I want to know more about

What are the regressive protocols which are alluded to in the REST reading? And why did they come about if they supposedly were inferior to HTTP?
