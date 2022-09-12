# AirBnB_EDA
EDA on AirBnB data for NYC


### Background
This is a dataset from https://www.kaggle.com/datasets/arianazmoudeh/airbnbopendata
It details listings for AirBnB rentals in NYC

### Objective:
This is primarily to perform EDA (Exploratory Data Analysis) and to run some visualizations as a refresher to myself. I will try to answer some questions (see below-TBD) and write about them.

### The Data:
The data consists of NYC AirBnB listings, with the following columns:
* 'id': Listing ID
* 'NAME': Listing Title
* 'host id': Host ID 
* 'host_identity_verified': Either confirmed host or unconfirmed host
* 'host name': Host Name
* 'neighbourhood group': NYC Borroughs (i.e Manhattan, Brooklyn, Bronx)
* 'neighbourhood': Specific neighborhoods (i.e. East Village, Harlem, Bushwick)
* 'lat': Lattidue of the listing
* 'long': Longitude of the listing
* 'country': United States
* 'country code': US
* 'instant_bookable': Whether the listing can be instantly book without prior host consent (True or False)
* 'cancellation_policy': What type of cancellation policy the listing has
* 'room type': Whether the room is entire home, private, or shared
* 'Construction year': Year of when the listing was constructed
* 'price': Nightly Price
* 'service fee': Service fee associated with the listing
* 'minimum nights': Number of minimum nights for the reservation
* 'number of reviews': Number of reviews for the listing
* 'last review': Date of the last review
* 'reviews per month': Average # of reviews per month
* 'review rate number': Star rating 1-5
* 'calculated host listings count': number of listings by Host
* 'availability 365': How often the listing is available in a year
* 'house_rules': rules of the home that the guest must abide by
* 'license': N/A, only two listings are not null, not useful.
 




### Analysis
The first step is to perform data cleaning as there were missing values and non-uniqueness and to investigate distribution of fields. For example, the column neighborhood group had nulls, and so I filled them in depending on what neighbourhood value it was (i.e. if neighbourhood was Williamsburg and neighbourhood group was missing, I filled it in as Brooklyn). I also removed columns where there was only 1 unique value (country, country code, license columns). The following are questions that will be asked (see jupyter notebook for analysis and findings):

* What are number of listings by Neighborhood Group/Neighborhood
* What about by Room Type
* Average Price by Room Type
* Average Price by Neighborhood Group/Neighborhood
* Correlation bw # of listings/review/rating?
* Correlation between Construction year and price?

### Conlcusion
Overall, this was just an exercise to get my feet wet again, and I chose this dataset as I am very familiar with AirBnB model since I used to work for a short term rental property management company that leveraged AirBnB to rent client's homes. The data, especially price, was not informative, as it was the listing price which does not equate to actual transaction price. Given that the average price was around 620 regardless of neighbourhood and room type was a dead giveaway. Normally Manhattan is the priciest as that is where tourists want to stay and private home/apt is higher than private room and shared room. The data did not suggest that, instead it showed roughly the same price regardless of neighbourhood or room type. 
