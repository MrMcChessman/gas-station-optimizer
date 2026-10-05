E36 = IMPORTHTML(join("","https://sitelocator.wexonline.com/search?sortByValue=Distance&sortDirectionValue=ASC&latitude=",G30,"&longitude=",H30,"&mapType=roadmap&mapZoom=12&sorting=false&code=&fuelTypeValue=Unleaded+Regular&radius=30"),"table",5)
# IMPORTHTML() sheet function used to call data from table 5 on sitelocator.wexonline.com.




G30 = SPLIT(GOOGLEMAPS_LATLONG(SUBSTITUTE(D4, CHAR(10), " ")),",")
# GOOGLEMAPS_LATLONG() Google Maps API call function to convert address-formatted location into Latitude & Longitude formatted location.




E32 = (8*TO_PURE_NUMBER(J36))+(substitute(GOOGLEMAPS_DISTANCE($D$4,H36)," mi", "")*$J$34*0.0333)
# GOOGLEMAPS_DISTANCE() Google Maps API call function used to display a more accurate distance for the user to drive to a given station.




W36 = to_pure_number(left(GOOGLEMAPS_DURATION($D$4,P36),2))
# GOOGLEMAPS_DURATION() Google Maps API call function used to display travel time between the user and a given station.




I7 = HYPERLINK(JOIN("","https://www.google.com/maps/dir/",$G$30,",",$H$30,"/",substitute(SUBSTITUTE(O36, CHAR(10), " ")," ","+"),"/@",V23,",",W23,"/"),JOIN(" - ",R36,N36))
# "https://www.google.com/maps/dir/..." Provides user with Google Maps directions for curated stations at a click.








