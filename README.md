# Web-Scraping

Got this from chat 
answer to the last question

#Finding the original Sun longitude
orig_long=df['ls'].loc[0]
orig_long

#find the next rows where longitude is equal the orig_long
same_long=df.loc[df['ls']==orig_long]
same_long

import datetime as dt
from datetime import timedelta
from datetime import datetime

a=same_long['terrestrial_date'].loc[0]
date_after_one_martial_year = same_long['terrestrial_date'].iloc[1]
one_martial_year= date_after_one_martial_year-a
print(f'In one Martial year, nearly ',one_martial_year,'pass on Earth')