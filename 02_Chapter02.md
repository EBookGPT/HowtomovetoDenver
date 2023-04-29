# Chapter 2: Researching Neighborhoods and Finding a Home

Gather 'round, dear reader! Before you move to Denver, it's crucial that you find the perfect neighborhood to suit your needs. A house is not just a house - it's a place you'll call home, where you'll build memories, and where you'll seek shelter from the hustle and bustle of the outside world. 

But where to begin? With so many neighborhoods to choose from, the task can seem quite daunting. Fear not, for I have come to guide you through this process with the grace and finesse of a ballerina floating through the air. 

In this chapter, we will embark on a journey together to explore Denver's neighborhoods. We will delve into their unique qualities, cultures, and quirks. We will also discuss how to find a home that fits your needs and budget.

But before we begin, let us first venture into the wondrous land of code. To start, we shall use Python's beautifulsoup4 library to scrape data from various websites and APIs to gather information on different neighborhoods in Denver. So grab your tea, sit back, and let's get started! 

```python
import requests
from bs4 import BeautifulSoup

url = 'https://www.neighborhoodscout.com/co/denver/real-estate'
response = requests.get(url)
soup = BeautifulSoup(response.content, "html.parser")

for row in soup.select(".table-responsive tr"):
    cells = row.find_all("td")
    if len(cells) == 6:
        name = cells[0].get_text(strip=True)
        median_home_price = cells[3].get_text(strip=True)
        population = cells[2].get_text(strip=True)
        print(name, median_home_price, population)
```

See how easy that was? With just a few lines of code, we can quickly gather data on various neighborhoods in Denver. So grab your top hat and monocle, dear reader, for we have much to explore together.
# Chapter 2: Researching Neighborhoods and Finding a Home

Welcome back, dear reader! I hope you enjoyed our adventure into the realm of code. Now, let us journey together into a world more surreal, more fantastical, and more bizarre than any code we could muster. 

You see, we have been presented with a great challenge - to find the perfect neighborhood for our Bostonian friends, who seek nothing more than a delicious brisket croissant in a city where such a delicacy is near impossible to find. 

As we wander through the streets of Denver, a curious cat with a wide grin crosses our path. "Good day, travelers!" the cat exclaims. "I see you are on a quest for the perfect home. Follow me, and I'll show you a land more magical than any you've seen before."

Intrigued, we follow the cat through a dark alley and into a hidden garden. There, we find a door that leads into a tunnel. The cat disappears, and we find ourselves falling through the tunnel, surrounded by psychedelic colors and shapes.

We land with a thud, and as we look around, we see ourselves in a room filled with doors - doors of all sizes, shapes, and colors. A sign reads, "Choose a door, any door, and you shall find the neighborhood of your dreams."

Without hesitation, we choose a door and step through. To our surprise, we find ourselves in a neighborhood full of energy - an urban oasis with a bustling downtown and plenty of activities. "Welcome to LoDo," a friendly passerby greets us. "This is the heart of Denver, where the city comes to life."

Excited, we explore the neighborhood, trying out every restaurant, coffee shop, and bar. But alas, no brisket croissant is to be found.

Undeterred, we return to the garden and find another door, leading us into a neighborhood filled with parks and greenery. "Welcome to Washington Park," a woman on a bicycle greets us. "This is where Denver's nature lovers come to unwind."

As we stroll through the park, enjoying the scenery and fresh air, we catch a whiff of something delicious. Could it be? Yes, it is - a food truck serving brisket croissants. Our Bostonian friends are overjoyed, and we know we have found their perfect neighborhood.

And so, dear reader, we have learned that finding the perfect neighborhood takes more than just research - it requires a sense of adventure, a willingness to explore, and a little bit of magic. So go forth and explore, and who knows what wonders you might uncover.
As we journey together through the surreal world of Denver, we encounter a mysterious cat who introduces us to a magical garden filled with doors of all shapes and colors. Each door leads to a unique neighborhood, but how do we choose which one is right for us?

To aid us in this quest, we turn to the power of Python and the beautifulsoup4 library. The Python code we used scraped data from a website (https://www.neighborhoodscout.com/co/denver/real-estate) which provides information on real estate pricing and neighborhood data for Denver. 

We used requests library to send an HTTP GET request to the URL `https://www.neighborhoodscout.com/co/denver/real-estate`. The server responds back with the HTML content of the web page. Then, we pass this HTML content to beautifulsoup4's `html.parser` to create a soup object.

Using a loop, we extracted relevant information from each row of the table present on the page, such as name, median home price and population, for each neighborhood under consideration. We printed this information for each neighborhood to better understand the neighborhoods in Denver and help us choose the perfect one for our Bostonian friends on their quest for the ultimate brisket croissant.

``` python
import requests
from bs4 import BeautifulSoup

# Send an HTTP GET request to the URL
url = 'https://www.neighborhoodscout.com/co/denver/real-estate'
response = requests.get(url)

# Create a soup object
soup = BeautifulSoup(response.content, 'html.parser')

# Extract information from each row of the table
for row in soup.select('.table-responsive tr'):
    cells = row.find_all('td')
    if len(cells) == 6:
        name = cells[0].get_text(strip=True)
        median_home_price = cells[3].get_text(strip=True)
        population = cells[2].get_text(strip=True)
        print(name, median_home_price, population)
```

By using the power of code, we were able to gather valuable information about each neighborhood in Denver, allowing us to make an informed decision on where to find the perfect home for our Bostonian friends.


[Next Chapter](03_Chapter03.md)