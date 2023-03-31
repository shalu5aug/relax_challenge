

## Case Study  : In this notebook,  I have investigated which factors are most important in determining future user adoption for a product.
Criteria for Defining an "adopted user" is who has logged into the product on three separate days in at least one seven day period.

### The data is available as two attached CSV files:
1. User table takehome_users.csv with data on 12,000 users who signed up for the product in the last two years.

   This table includes:

   a.  name: the user's name
 
   b.  object_id: the user's id
 
   c.  email: email address
 
   d. creation_source: how their account was created. This takes on one
      of 5 values:
 
      ○ PERSONAL_PROJECTS: invited to join another user's personal workspace
  
      ○ GUEST_INVITE: invited to an organization as a guest (limited permissions)
  
      ○ ORG_INVITE: invited to an organization (as a full member)
  
      ○ SIGNUP: signed up via the website
  
      ○ SIGNUP_GOOGLE_AUTH: signed up using Google
        Authentication (using a Google email account for their login
        id)
    
   e. creation_time: when they created their account
 
   f. last_session_creation_time: unix timestamp of last login
 
   g. opted_in_to_mailing_list: whether they have opted into receiving
      marketing emails
    
   h. enabled_for_marketing_drip: whether they are on the regular
    marketing email drip
    
   i. org_id: the organization (group of users) they belong to
 
   j. invited_by_user_id: which user invited them to join (if applicable).

2. takehome_user_engagement.csv  that has a row for each day that a user logged into the product.

the dataset contains information about 8,823 users among which 1,656 are adopted users.


As per the analysis I found that the most important feature in determining user adoption is “total login time” i.e history of user the time from user signed up and user last login time.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/83147951/228968345-f12ad21d-3fdb-4919-8852-ebd901523b5d.png">

Correlation between all the features in dataset

<img width="337" alt="image" src="https://user-images.githubusercontent.com/83147951/228968292-70cd3b2d-96e5-481b-8c12-0ad58b39309f.png">


The other important feature is the ‘source of creation’. Users invited by other users and users signed up to do personal projects are more likely to be adopted users:
 
Percentage of adopted users with source of creation:
   
 <img width="468" alt="image" src="https://user-images.githubusercontent.com/83147951/228967844-0f040f0a-a0e2-4a85-b15e-5010c68e92e1.png">
There are 22% of adopted who are invited by guests , 34% who are invited by some org and 10% who signed up for personal projects

Based on the above findings , I would recommend the good way to grow adopted users is to offer some incentives to users who once signed up to use the product and encourage existing users to invite others users .


Files information :
  
Folder relax_corp contains dataset and notebook files : relax_challenge.ipynb contains the EDA and modelling part  and relax_challenge.pdf contains the answers of the Relax challenge assignment
