# Source
Mattia Giovanni Campana (1)
 Franca Delmastro (1)

1-- Institute for Informatics and Telematics
 National Research Council of Italy (Pisa
 Italy)

# Data Set Information

We used the [ContextKit framwork](https://contextkit.github.io/) to collect a **real labeled dataset** containing heterogeneous sensing data derived from personal mobile devices in order to characterize the user physical context (i.e., her situation).

In details, we used the following sensors:

- User's gait
- Running applications
- Weather conditions
- Audio info (e.g.
 ringtones volumes)
- Battery status (i.e.
 battery level and if the device is recharging)
- Bluetooth (device connected and in the nearby)
- Display status (e.g.
 on/off) and rotation angle
- Location
- Wi-Fi
- Physical Sensors (i.e.
 light
 accelerometer
 gravity
 gyroscope
 linear acceleration
 orientation
 and proximity)
- Multimedia (photo and video)

In order to obtain a real dataset
 we avoid to perform the data acquisition in controlled environments (e.g.
  lab)
 and we enrolled 3 voluntary users equipped with heterogeneous commercial smartphones
 with different characteristics and sensors.
In details
 `user_1` used a Nexus 5 with Android 6.0.1
 `user_2` used a Xiaomi Mi 5 with Android 7.1.2
 and `user_3` used a Reader P10 with Android 6.0.

Each volunteer used our sensing application for a period of two weeks
 during which she specified her daily-life situations from the following list of predefined labels:

- Break
- Cinema
- Freetime
- Home
- Lunch break
- Nightlife
- Gym
- Restaurant
- Shopping
- Sleep
- Theater
- Working

# Attributes Information
We used the One-hot encoding to create the feature vectors in our dataset.
Each vector is composed by the following 1331 features:

Time
---
Information about when the sensors reading has been performed.
- weekday
- weekend
- morning
- afternoon
- evening
- night

Activity Recognition
---

User's current actity according to the [Android Activity Recognition API](https://developers.google.com/android/reference/com/google/android/gms/location/ActivityRecognitionClient).

- activity_rec_in_vehicle
- activity_rec_on_bicycle
- activity_rec_on_foot
- activity_rec_running
- activity_rec_still
- activity_rec_tilting
- activity_rec_walking
- activity_rec_unknown

Running Applications 
---

Categories of the running applications. The categories have been downloaded from the [Google Play Store](https://play.google.com/store).

- ANDROID_WEAR
- ART_AND_DESIGN
- AUTO_AND_VEHICLES
- BEAUTY
- BOOKS_AND_REFERENCE
- BUSINESS
- COMICS
- COMMUNICATION
- DATING
- EDUCATION
- ENTERTAINMENT
- EVENTS
- FAMILY_ACTION
- FAMILY_BRAINGAMES
- FAMILY_CREATE
- FAMILY_EDUCATION
- FAMILY_MUSICVIDEO
- FAMILY_PRETEND
- FINANCE
- FOOD_AND_DRINK
- GAME_ACTION
- GAME_ADVENTURE
- GAME_ARCADE
- GAME_BOARD
- GAME_CARD
- GAME_CASINO
- GAME_CASUAL
- GAME_EDUCATIONAL
- GAME_MUSIC
- GAME_PUZZLE
- GAME_RACING
- GAME_ROLE_PLAYING
- GAME_SIMULATION
- GAME_SPORTS
- GAME_STRATEGY
- GAME_TRIVIA
- GAME_WORD
- HEALTH_AND_FITNESS
- HOUSE_AND_HOME
- LIBRARIES_AND_DEMO
- LIFESTYLE
- MAPS_AND_NAVIGATION
- MEDICAL
- MUSIC_AND_AUDIO
- NEWS_AND_MAGAZINES
- PARENTING
- PERSONALIZATION
- PHOTOGRAPHY
- PRODUCTIVITY
- SHOPPING
- SOCIAL
- SPORTS
- TOOLS
- TRAVEL_AND_LOCAL
- VIDEO_PLAYERS
- WEATHER

Weather Conditions 
---

Weather conditions (e.g., raining/sunny, temperature, and wind) downloaded from the [OpenWeatherMap service](https://openweathermap.org) based on the user's location.
See the [API documentation](https://openweathermap.org/current) for more information.

- weather_code_200
- weather_code_201
- weather_code_202
- weather_code_210
- weather_code_211
- weather_code_212
- weather_code_221
- weather_code_230
- weather_code_231
- weather_code_232
- weather_code_300
- weather_code_301
- weather_code_302
- weather_code_310
- weather_code_311
- weather_code_312
- weather_code_313
- weather_code_314
- weather_code_321
- weather_code_500
- weather_code_501
- weather_code_502
- weather_code_503
- weather_code_504
- weather_code_511
- weather_code_520
- weather_code_521
- weather_code_522
- weather_code_531
- weather_code_600
- weather_code_601
- weather_code_602
- weather_code_611
- weather_code_612
- weather_code_615
- weather_code_616
- weather_code_620
- weather_code_621
- weather_code_622
- weather_code_701
- weather_code_711
- weather_code_721
- weather_code_731
- weather_code_741
- weather_code_751
- weather_code_761
- weather_code_762
- weather_code_771
- weather_code_781
- weather_code_800
- weather_code_801
- weather_code_802
- weather_code_803
- weather_code_804
- weather_temp
- weather_temp_min
- weather_temp_max
- weather_humidity
- weather_pressure
- weather_wind_speed
- weather_wind_direction
- weather_cloudiness

Audio
---

Audio information given by the [Android AudioManager](https://developer.android.com/reference/android/media/AudioManager).

- audio_ringer_mode_silent
- audio_ringer_mode_vibrate
- audio_ringer_mode_normal
- audio_alarm_volume
- audio_music_volume
- audio_notification_volume
- audio_ring_volume
- audio_bt_sco_on
- audio_mic_mute
- audio_music_active
- audio_speaker_on
- audio_headset_on

Battery
---

Battery level and charging state (see the [Android documentation](https://developer.android.com/training/monitoring-device-state/battery-monitoring)).

- battery_unplugged
- battery_plugged_ac
- battery_plugged_usb
- battery_plugged_wireless

Bluetooth Connections
---

Major class ID of the first 5 Bluetooth devices connected to the user's smartphone (see the [Android Bluetooth Class Device Documentation](https://developer.android.com/reference/android/bluetooth/BluetoothClass.Device.Major).

- bt_con_1_audio_video
- bt_con_1_computer
- bt_con_1_health
- bt_con_1_imaging
- bt_con_1_misc
- bt_con_1_networking
- bt_con_1_peripheral
- bt_con_1_phone
- bt_con_1_toy
- bt_con_1_uncategorized
- bt_con_1_wearable
- bt_con_2_audio_video
- bt_con_2_computer
- bt_con_2_health
- bt_con_2_imaging
- bt_con_2_misc
- bt_con_2_networking
- bt_con_2_peripheral
- bt_con_2_phone
- bt_con_2_toy
- bt_con_2_uncategorized
- bt_con_2_wearable
- bt_con_3_computer
- bt_con_3_health
- bt_con_3_imaging
- bt_con_3_misc
- bt_con_3_networking
- bt_con_3_peripheral
- bt_con_3_phone
- bt_con_3_toy
- bt_con_3_uncategorized
- bt_con_3_wearable
- bt_con_4_audio_video
- bt_con_4_computer
- bt_con_4_health
- bt_con_4_imaging
- bt_con_4_misc
- bt_con_4_networking
- bt_con_4_peripheral
- bt_con_4_phone
- bt_con_4_toy
- bt_con_4_uncategorized
- bt_con_4_wearable
- bt_con_5_audio_video
- bt_con_5_computer
- bt_con_5_health
- bt_con_5_imaging
- bt_con_5_misc
- bt_con_5_networking
- bt_con_5_peripheral
- bt_con_5_phone
- bt_con_5_toy
- bt_con_5_uncategorized
- bt_con_5_wearable

Bluetooth Devices in Proximity
---

Major class ID of the first 5 Bluetooth devices in proximity (see the [Android Bluetooth Class Device Documentation](https://developer.android.com/reference/android/bluetooth/BluetoothClass.Device.Major).

- bt_scan_1_audio_video
- bt_scan_1_computer
- bt_scan_1_health
- bt_scan_1_imaging
- bt_scan_1_misc
- bt_scan_1_networking
- bt_scan_1_peripheral
- bt_scan_1_phone
- bt_scan_1_toy
- bt_scan_1_uncategorized
- bt_scan_1_wearable
- bt_scan_2_audio_video
- bt_scan_2_computer
- bt_scan_2_health
- bt_scan_2_imaging
- bt_scan_2_misc
- bt_scan_2_networking
- bt_scan_2_peripheral
- bt_scan_2_phone
- bt_scan_2_toy
- bt_scan_2_uncategorized
- bt_scan_2_wearable
- bt_scan_3_computer
- bt_scan_3_health
- bt_scan_3_imaging
- bt_scan_3_misc
- bt_scan_3_networking
- bt_scan_3_peripheral
- bt_scan_3_phone
- bt_scan_3_toy
- bt_scan_3_uncategorized
- bt_scan_3_wearable
- bt_scan_4_audio_video
- bt_scan_4_computer
- bt_scan_4_health
- bt_scan_4_imaging
- bt_scan_4_misc
- bt_scan_4_networking
- bt_scan_4_peripheral
- bt_scan_4_phone
- bt_scan_4_toy
- bt_scan_4_uncategorized
- bt_scan_4_wearable
- bt_scan_5_audio_video
- bt_scan_5_computer
- bt_scan_5_health
- bt_scan_5_imaging
- bt_scan_5_misc
- bt_scan_5_networking
- bt_scan_5_peripheral
- bt_scan_5_phone
- bt_scan_5_toy
- bt_scan_5_uncategorized
- bt_scan_5_wearable

Display Status
---

Status and orientation of the smartphone's display ([ref](https://developer.android.com/reference/android/view/Display)).

- display_status_unknown
- display_status_off
- display_status_on
- display_status_doze
- display_status_doze_suspended
- display_status_vr_mode
- display_status_on_suspended
- display_rotation_0
- display_rotation_90
- display_rotation_180
- display_rotation_270

Location
---

Geographical coordinates of the user's location.
In addition, we used the [Foursquare Places APIs](https://developer.foursquare.com/places-api) to retrieve the category of the most probable venue accordingto the location's coordinates.

- location_lat
- location_lon
- Arts & Entertainment
- Amphitheater
- Aquarium
- Arcade
- Art Gallery
- Bowling Alley
- Casino
- Circus
- Comedy Club
- Concert Hall
- Country Dance Club
- Disc Golf
- Exhibit
- General Entertainment
- Go Kart Track
- Historic Site
- Karaoke Box
- Laser Tag
- Memorial Site
- Mini Golf
- Movie Theater
- Drive-in Theater
- Indie Movie Theater
- Multiplex
- Museum
- Art Museum
- Erotic Museum
- History Museum
- Planetarium
- Science Museum
- Music Venue
- Jazz Club
- Piano Bar
- Rock Club
- Pachinko Parlor
- Performing Arts Venue
- Dance Studio
- Indie Theater
- Opera House
- Theater
- Pool Hall
- Public Art
- Outdoor Sculpture
- Street Art
- Racecourse
- Racetrack
- Roller Rink
- Salsa Club
- Samba School
- Stadium
- Baseball Stadium
- Basketball Stadium
- Cricket Ground
- Football Stadium
- Hockey Arena
- Rugby Stadium
- Soccer Stadium
- Tennis Stadium
- Track Stadium
- Theme Park
- Theme Park Ride / Attraction
- Tour Provider
- Water Park
- Zoo
- Zoo Exhibit
- College & University
- College Academic Building
- College Arts Building
- College Communications Building
- College Engineering Building
- College History Building
- College Math Building
- College Science Building
- College Technology Building
- College Administrative Building
- College Auditorium
- College Bookstore
- College Cafeteria
- College Classroom
- College Gym
- College Lab
- College Library
- College Quad
- College Rec Center
- College Residence Hall
- College Stadium
- College Baseball Diamond
- College Basketball Court
- College Cricket Pitch
- College Football Field
- College Hockey Rink
- College Soccer Field
- College Tennis Court
- College Track
- College Theater
- Community College
- Fraternity House
- General College & University
- Law School
- Medical School
- Sorority House
- Student Center
- Trade School
- University
- Event
- Christmas Market
- Conference
- Convention
- Festival
- Line / Queue
- Music Festival
- Other Event
- Parade
- Stoop Sale
- Street Fair
- Food
- Afghan Restaurant
- African Restaurant
- Ethiopian Restaurant
- American Restaurant
- New American Restaurant
- Asian Restaurant
- Burmese Restaurant
- Cambodian Restaurant
- Chinese Restaurant
- Anhui Restaurant
- Beijing Restaurant
- Cantonese Restaurant
- Cha Chaan Teng
- Chinese Aristocrat Restaurant
- Chinese Breakfast Place
- Dim Sum Restaurant
- Dongbei Restaurant
- Fujian Restaurant
- Guizhou Restaurant
- Hainan Restaurant
- Hakka Restaurant
- Henan Restaurant
- Hong Kong Restaurant
- Huaiyang Restaurant
- Hubei Restaurant
- Hunan Restaurant
- Imperial Restaurant
- Jiangsu Restaurant
- Jiangxi Restaurant
- Macanese Restaurant
- Manchu Restaurant
- Peking Duck Restaurant
- Shaanxi Restaurant
- Shandong Restaurant
- Shanghai Restaurant
- Shanxi Restaurant
- Szechuan Restaurant
- Taiwanese Restaurant
- Tianjin Restaurant
- Xinjiang Restaurant
- Yunnan Restaurant
- Zhejiang Restaurant
- Filipino Restaurant
- Himalayan Restaurant
- Hotpot Restaurant
- Indonesian Restaurant
- Acehnese Restaurant
- Balinese Restaurant
- Betawinese Restaurant
- Indonesian Meatball Place
- Javanese Restaurant
- Manadonese Restaurant
- Padangnese Restaurant
- Sundanese Restaurant
- Japanese Restaurant
- Donburi Restaurant
- Japanese Curry Restaurant
- Kaiseki Restaurant
- Kushikatsu Restaurant
- Monjayaki Restaurant
- Nabe Restaurant
- Okonomiyaki Restaurant
- Ramen Restaurant
- Shabu-Shabu Restaurant
- Soba Restaurant
- Sukiyaki Restaurant
- Sushi Restaurant
- Takoyaki Place
- Tempura Restaurant
- Tonkatsu Restaurant
- Udon Restaurant
- Unagi Restaurant
- Wagashi Place
- Yakitori Restaurant
- Yoshoku Restaurant
- Korean Restaurant
- Bossam/Jokbal Restaurant
- Bunsik Restaurant
- Gukbap Restaurant
- Janguh Restaurant
- Samgyetang Restaurant
- Malay Restaurant
- Mongolian Restaurant
- Noodle House
- Satay Restaurant
- Thai Restaurant
- Som Tum Restaurant
- Tibetan Restaurant
- Vietnamese Restaurant
- Australian Restaurant
- Austrian Restaurant
- BBQ Joint
- Bagel Shop
- Bakery
- Belgian Restaurant
- Bistro
- Breakfast Spot
- Bubble Tea Shop
- Buffet
- Burger Joint
- Cafeteria
- Café
- Cajun / Creole Restaurant
- Caribbean Restaurant
- Cuban Restaurant
- Caucasian Restaurant
- Coffee Shop
- Comfort Food Restaurant
- Creperie
- Czech Restaurant
- Deli / Bodega
- Dessert Shop
- Cupcake Shop
- Frozen Yogurt Shop
- Ice Cream Shop
- Pastry Shop
- Pie Shop
- Diner
- Donut Shop
- Dumpling Restaurant
- Dutch Restaurant
- Eastern European Restaurant
- Belarusian Restaurant
- Bosnian Restaurant
- Bulgarian Restaurant
- Romanian Restaurant
- Tatar Restaurant
- English Restaurant
- Falafel Restaurant
- Fast Food Restaurant
- Fish & Chips Shop
- Fondue Restaurant
- Food Court
- Food Stand
- Food Truck
- French Restaurant
- Alsatian Restaurant
- Auvergne Restaurant
- Basque Restaurant
- Brasserie
- Breton Restaurant
- Burgundian Restaurant
- Catalan Restaurant
- Ch'ti Restaurant
- Corsican Restaurant
- Estaminet
- Labour Canteen
- Lyonese Bouchon
- Norman Restaurant
- Provençal Restaurant
- Savoyard Restaurant
- Southwestern French Restaurant
- Fried Chicken Joint
- Friterie
- Gastropub
- German Restaurant
- Apple Wine Pub
- Bavarian Restaurant
- Bratwurst Joint
- Currywurst Joint
- Franconian Restaurant
- German Pop-Up Restaurant
- Palatine Restaurant
- Rhenisch Restaurant
- Schnitzel Restaurant
- Silesian Restaurant
- Swabian Restaurant
- Gluten-free Restaurant
- Greek Restaurant
- Bougatsa Shop
- Cretan Restaurant
- Fish Taverna
- Grilled Meat Restaurant
- Kafenio
- Magirio
- Meze Restaurant
- Modern Greek Restaurant
- Ouzeri
- Patsa Restaurant
- Souvlaki Shop
- Taverna
- Tsipouro Restaurant
- Halal Restaurant
- Hawaiian Restaurant
- Hot Dog Joint
- Hungarian Restaurant
- Indian Restaurant
- Andhra Restaurant
- Awadhi Restaurant
- Bengali Restaurant
- Chaat Place
- Chettinad Restaurant
- Dhaba
- Dosa Place
- Goan Restaurant
- Gujarati Restaurant
- Hyderabadi Restaurant
- Indian Chinese Restaurant
- Indian Sweet Shop
- Irani Cafe
- Jain Restaurant
- Karnataka Restaurant
- Kerala Restaurant
- Maharashtrian Restaurant
- Mughlai Restaurant
- Multicuisine Indian Restaurant
- North Indian Restaurant
- Northeast Indian Restaurant
- Parsi Restaurant
- Punjabi Restaurant
- Rajasthani Restaurant
- South Indian Restaurant
- Udupi Restaurant
- Irish Pub
- Italian Restaurant
- Abruzzo Restaurant
- Agriturismo
- Aosta Restaurant
- Basilicata Restaurant
- Calabria Restaurant
- Campanian Restaurant
- Emilia Restaurant
- Friuli Restaurant
- Ligurian Restaurant
- Lombard Restaurant
- Malga
- Marche Restaurant
- Molise Restaurant
- Piadineria
- Piedmontese Restaurant
- Puglia Restaurant
- Romagna Restaurant
- Roman Restaurant
- Sardinian Restaurant
- Sicilian Restaurant
- South Tyrolean Restaurant
- Trattoria/Osteria
- Trentino Restaurant
- Tuscan Restaurant
- Umbrian Restaurant
- Veneto Restaurant
- Jewish Restaurant
- Kosher Restaurant
- Juice Bar
- Kebab Restaurant
- Latin American Restaurant
- Arepa Restaurant
- Empanada Restaurant
- Salvadoran Restaurant
- South American Restaurant
- Argentinian Restaurant
- Brazilian Restaurant
- Acai House
- Baiano Restaurant
- Central Brazilian Restaurant
- Churrascaria
- Empada House
- Goiano Restaurant
- Mineiro Restaurant
- Northeastern Brazilian Restaurant
- Northern Brazilian Restaurant
- Pastelaria
- Southeastern Brazilian Restaurant
- Southern Brazilian Restaurant
- Tapiocaria
- Colombian Restaurant
- Peruvian Restaurant
- Venezuelan Restaurant
- Mac & Cheese Joint
- Mediterranean Restaurant
- Moroccan Restaurant
- Mexican Restaurant
- Botanero
- Burrito Place
- Taco Place
- Tex-Mex Restaurant
- Yucatecan Restaurant
- Middle Eastern Restaurant
- Israeli Restaurant
- Kurdish Restaurant
- Lebanese Restaurant
- Persian Restaurant
- Ash and Haleem Place
- Dizi Place
- Gilaki Restaurant
- Jegaraki
- Tabbakhi
- Modern European Restaurant
- Molecular Gastronomy Restaurant
- Pakistani Restaurant
- Pet Café
- Pizza Place
- Polish Restaurant
- Portuguese Restaurant
- Poutine Place
- Restaurant
- Russian Restaurant
- Blini House
- Pelmeni House
- Salad Place
- Sandwich Place
- Scandinavian Restaurant
- Scottish Restaurant
- Seafood Restaurant
- Slovak Restaurant
- Snack Place
- Soup Place
- Southern / Soul Food Restaurant
- Spanish Restaurant
- Paella Restaurant
- Tapas Restaurant
- Sri Lankan Restaurant
- Steakhouse
- Swiss Restaurant
- Tea Room
- Theme Restaurant
- Truck Stop
- Turkish Restaurant
- Borek Place
- Cigkofte Place
- Doner Restaurant
- Gozleme Place
- Kofte Place
- Kokoreç Restaurant
- Kumpir Restaurant
- Kumru Restaurant
- Manti Place
- Meyhane
- Pide Place
- Pilavcı
- Söğüş Place
- Tantuni Restaurant
- Turkish Coffeehouse
- Turkish Home Cooking Restaurant
- Çöp Şiş Place
- Ukrainian Restaurant
- Varenyky restaurant
- West-Ukrainian Restaurant
- Vegetarian / Vegan Restaurant
- Wings Joint
- Nightlife Spot
- Bar
- Beach Bar
- Beer Bar
- Beer Garden
- Champagne Bar
- Cocktail Bar
- Dive Bar
- Gay Bar
- Hookah Bar
- Hotel Bar
- Karaoke Bar
- Pub
- Sake Bar
- Speakeasy
- Sports Bar
- Tiki Bar
- Whisky Bar
- Wine Bar
- Brewery
- Lounge
- Night Market
- Nightclub
- Other Nightlife
- Strip Club
- Outdoors & Recreation
- Athletics & Sports
- Badminton Court
- Baseball Field
- Basketball Court
- Bowling Green
- Curling Ice
- Golf Course
- Golf Driving Range
- Gym / Fitness Center
- Boxing Gym
- Climbing Gym
- Cycle Studio
- Gym Pool
- Gymnastics Gym
- Gym
- Martial Arts Dojo
- Outdoor Gym
- Pilates Studio
- Track
- Weight Loss Center
- Yoga Studio
- Hockey Field
- Hockey Rink
- Paintball Field
- Rugby Pitch
- Skate Park
- Skating Rink
- Soccer Field
- Sports Club
- Squash Court
- Tennis Court
- Volleyball Court
- Bathing Area
- Bay
- Beach
- Nudist Beach
- Surf Spot
- Bike Trail
- Botanical Garden
- Bridge
- Campground
- Canal Lock
- Canal
- Castle
- Cave
- Cemetery
- Dive Spot
- Dog Run
- Farm
- Field
- Fishing Spot
- Forest
- Fountain
- Garden
- Gun Range
- Harbor / Marina
- Hot Spring
- Indoor Play Area
- Island
- Lake
- Lighthouse
- Mountain Hut
- Mountain
- National Park
- Nature Preserve
- Other Great Outdoors
- Palace
- Park
- Pedestrian Plaza
- Playground
- Plaza
- Pool
- Rafting
- Recreation Center
- Reservoir
- River
- Rock Climbing Spot
- Scenic Lookout
- Sculpture Garden
- Ski Area
- Apres Ski Bar
- Ski Chairlift
- Ski Chalet
- Ski Lodge
- Ski Trail
- Skydiving Drop Zone
- Stables
- States & Municipalities
- City
- County
- Country
- Neighborhood
- State
- Town
- Village
- Summer Camp
- Trail
- Tree
- Vineyard
- Volcano
- Waterfall
- Waterfront
- Well
- Professional & Other Places
- Animal Shelter
- Art Studio
- Auditorium
- Ballroom
- Building
- Business Center
- Club House
- Community Center
- Convention Center
- Meeting Room
- Cultural Center
- Distillery
- Distribution Center
- Event Space
- Outdoor Event Space
- Factory
- Fair
- Funeral Home
- Government Building
- Capitol Building
- City Hall
- Courthouse
- Embassy / Consulate
- Fire Station
- Monument / Landmark
- Police Station
- Town Hall
- Industrial Estate
- Laboratory
- Library
- Medical Center
- Acupuncturist
- Alternative Healer
- Chiropractor
- Dentist's Office
- Doctor's Office
- Emergency Room
- Eye Doctor
- Hospital
- Hospital Ward
- Maternity Clinic
- Medical Lab
- Mental Health Office
- Nutritionist
- Physical Therapist
- Rehab Center
- Urgent Care Center
- Veterinarian
- Military Base
- Non-Profit
- Observatory
- Office
- Advertising Agency
- Campaign Office
- Conference Room
- Corporate Amenity
- Corporate Cafeteria
- Corporate Coffee Shop
- Coworking Space
- Tech Startup
- Parking
- Post Office
- Power Plant
- Prison
- Radio Station
- Recruiting Agency
- Research Station
- School
- Adult Education Center
- Circus School
- Cooking School
- Driving School
- Elementary School
- Flight School
- High School
- Language School
- Middle School
- Music School
- Nursery School
- Preschool
- Private School
- Religious School
- Swim School
- Social Club
- Spiritual Center
- Buddhist Temple
- Cemevi
- Church
- Confucian Temple
- Hindu Temple
- Kingdom Hall
- Monastery
- Mosque
- Prayer Room
- Shrine
- Synagogue
- Temple
- Terreiro
- TV Station
- Voting Booth
- Warehouse
- Waste Facility
- Wedding Hall
- Winery
- Residence
- Assisted Living
- Home (private)
- Housing Development
- Residential Building (Apartment / Condo)
- Trailer Park
- Shop & Service
- ATM
- Adult Boutique
- Antique Shop
- Arts & Crafts Store
- Astrologer
- Auto Dealership
- Auto Garage
- Auto Workshop
- Automotive Shop
- Baby Store
- Bank
- Bath House
- Batik Shop
- Betting Shop
- Big Box Store
- Bike Shop
- Board Shop
- Bookstore
- Bridal Shop
- Business Service
- Camera Store
- Candy Store
- Car Wash
- Carpet Store
- Check Cashing Service
- Child Care Service
- Daycare
- Chocolate Shop
- Clothing Store
- Accessories Store
- Boutique
- Kids Store
- Lingerie Store
- Men's Store
- Shoe Store
- Women's Store
- Comic Shop
- Construction & Landscaping
- Convenience Store
- Cosmetics Shop
- Costume Shop
- Credit Union
- Currency Exchange
- Department Store
- Design Studio
- Discount Store
- Dive Shop
- Drugstore
- Dry Cleaner
- EV Charging Station
- Electronics Store
- Entertainment Service
- Event Service
- Fabric Shop
- Film Studio
- Financial or Legal Service
- Fireworks Store
- Fishing Store
- Flea Market
- Floating Market
- Flower Shop
- Food & Drink Shop
- Beer Store
- Butcher
- Cheese Shop
- Dairy Store
- Farmers Market
- Fish Market
- Food Service
- Gourmet Shop
- Grocery Store
- Health Food Store
- Kuruyemişçi
- Liquor Store
- Organic Grocery
- Sausage Shop
- Street Food Gathering
- Supermarket
- Turşucu
- Wine Shop
- Frame Store
- Fruit & Vegetable Store
- Furniture / Home Store
- Lighting Store
- Gaming Cafe
- Garden Center
- Gas Station
- Gift Shop
- Gun Shop
- Hardware Store
- Health & Beauty Service
- Herbs & Spices Store
- Hobby Shop
- Home Service
- Hunting Supply
- IT Services
- Insurance Office
- Internet Cafe
- Jewelry Store
- Kitchen Supply Store
- Knitting Store
- Laundromat
- Laundry Service
- Lawyer
- Leather Goods Store
- Locksmith
- Lottery Retailer
- Luggage Store
- Marijuana Dispensary
- Market
- Massage Studio
- Mattress Store
- Medical Supply Store
- Miscellaneous Shop
- Mobile Phone Shop
- Mobility Store
- Motorcycle Shop
- Motorsports Shop
- Music Store
- Nail Salon
- Newsstand
- Optical Shop
- Other Repair Shop
- Outdoor Supply Store
- Outlet Mall
- Outlet Store
- Paper / Office Supplies Store
- Pawn Shop
- Perfume Shop
- Pet Service
- Pet Store
- Pharmacy
- Photography Lab
- Photography Studio
- Piercing Parlor
- Pop-Up Shop
- Print Shop
- Public Bathroom
- Real Estate Office
- Record Shop
- Recording Studio
- Recycling Facility
- Rental Service
- Salon / Barbershop
- Sauna / Steam Room
- Shipping Store
- Shoe Repair
- Shopping Mall
- Shopping Plaza
- Ski Shop
- Smoke Shop
- Smoothie Shop
- Souvenir Shop
- Spa
- Sporting Goods Shop
- Stationery Store
- Storage Facility
- Supplement Shop
- Tailor Shop
- Tanning Salon
- Tattoo Parlor
- Thrift / Vintage Store
- Toy / Game Store
- Travel Agency
- Used Bookstore
- Vape Store
- Video Game Store
- Video Store
- Warehouse Store
- Watch Shop
- Travel & Transport
- Airport
- Airport Food Court
- Airport Gate
- Airport Lounge
- Airport Service
- Airport Terminal
- Airport Tram
- Baggage Claim
- Plane
- Baggage Locker
- Bike Rental / Bike Share
- Boat Rental
- Boat or Ferry
- Border Crossing
- Bus Station
- Bus Line
- Bus Stop
- Cable Car
- Cruise
- Duty-free Shop
- General Travel
- Heliport
- Hotel
- Bed & Breakfast
- Boarding House
- Hostel
- Hotel Pool
- Motel
- Resort
- Roof Deck
- Vacation Rental
- Intersection
- Light Rail Station
- Metro Station
- Moving Target
- Pier
- Port
- RV Park
- Rental Car Location
- Rest Area
- Road
- Taxi Stand
- Taxi
- Toll Booth
- Toll Plaza
- Tourist Information Center
- Train Station
- Platform
- Train
- Tram Station
- Transportation Service
- Travel Lounge
- Tunnel


Wi-Fi
---
This feature indicates if the devices was connected to a Wi-Fi Access Point.
- wifi_connected

Physical Sensors
---

For each sensor, we obtained 200 reads and reported some basic statistics (i.e., min, max, mean, quadratic mean, and 25/50/75/100 percentiles).

- sensor_light_min
- sensor_light_max
- sensor_light_mean
- sensor_light_quadratic_mean
- sensor_light_25_percentile
- sensor_light_50_percentile
- sensor_light_75_percentile
- sensor_light_100_percentile
- sensor_accelerometer_x_min
- sensor_accelerometer_x_max
- sensor_accelerometer_x_mean
- sensor_accelerometer_x_quadratic_mean
- sensor_accelerometer_x_25_percentile
- sensor_accelerometer_x_50_percentile
- sensor_accelerometer_x_75_percentile
- sensor_accelerometer_x_100_percentile
- sensor_accelerometer_y_min
- sensor_accelerometer_y_max
- sensor_accelerometer_y_mean
- sensor_accelerometer_y_quadratic_mean
- sensor_accelerometer_y_25_percentile
- sensor_accelerometer_y_50_percentile
- sensor_accelerometer_y_75_percentile
- sensor_accelerometer_y_100_percentile
- sensor_accelerometer_z_min
- sensor_accelerometer_z_max
- sensor_accelerometer_z_mean
- sensor_accelerometer_z_quadratic_mean
- sensor_accelerometer_z_25_percentile
- sensor_accelerometer_z_50_percentile
- sensor_accelerometer_z_75_percentile
- sensor_accelerometer_z_100_percentile
- sensor_gravity_x_min
- sensor_gravity_x_max
- sensor_gravity_x_mean
- sensor_gravity_x_quadratic_mean
- sensor_gravity_x_25_percentile
- sensor_gravity_x_50_percentile
- sensor_gravity_x_75_percentile
- sensor_gravity_x_100_percentile
- sensor_gravity_y_min
- sensor_gravity_y_max
- sensor_gravity_y_mean
- sensor_gravity_y_quadratic_mean
- sensor_gravity_y_25_percentile
- sensor_gravity_y_50_percentile
- sensor_gravity_y_75_percentile
- sensor_gravity_y_100_percentile
- sensor_gravity_z_min
- sensor_gravity_z_max
- sensor_gravity_z_mean
- sensor_gravity_z_quadratic_mean
- sensor_gravity_z_25_percentile
- sensor_gravity_z_50_percentile
- sensor_gravity_z_75_percentile
- sensor_gravity_z_100_percentile
- sensor_gyroscope_x_min
- sensor_gyroscope_x_max
- sensor_gyroscope_x_mean
- sensor_gyroscope_x_quadratic_mean
- sensor_gyroscope_x_25_percentile
- sensor_gyroscope_x_50_percentile
- sensor_gyroscope_x_75_percentile
- sensor_gyroscope_x_100_percentile
- sensor_gyroscope_y_min
- sensor_gyroscope_y_max
- sensor_gyroscope_y_mean
- sensor_gyroscope_y_quadratic_mean
- sensor_gyroscope_y_25_percentile
- sensor_gyroscope_y_50_percentile
- sensor_gyroscope_y_75_percentile
- sensor_gyroscope_y_100_percentile
- sensor_gyroscope_z_min
- sensor_gyroscope_z_max
- sensor_gyroscope_z_mean
- sensor_gyroscope_z_quadratic_mean
- sensor_gyroscope_z_25_percentile
- sensor_gyroscope_z_50_percentile
- sensor_gyroscope_z_75_percentile
- sensor_gyroscope_z_100_percentile
- sensor_linear_acc_x_min
- sensor_linear_acc_x_max
- sensor_linear_acc_x_mean
- sensor_linear_acc_x_quadratic_mean
- sensor_linear_acc_x_25_percentile
- sensor_linear_acc_x_50_percentile
- sensor_linear_acc_x_75_percentile
- sensor_linear_acc_x_100_percentile
- sensor_linear_acc_y_min
- sensor_linear_acc_y_max
- sensor_linear_acc_y_mean
- sensor_linear_acc_y_quadratic_mean
- sensor_linear_acc_y_25_percentile
- sensor_linear_acc_y_50_percentile
- sensor_linear_acc_y_75_percentile
- sensor_linear_acc_y_100_percentile
- sensor_linear_acc_z_min
- sensor_linear_acc_z_max
- sensor_linear_acc_z_mean
- sensor_linear_acc_z_quadratic_mean
- sensor_linear_acc_z_25_percentile
- sensor_linear_acc_z_50_percentile
- sensor_linear_acc_z_75_percentile
- sensor_linear_acc_z_100_percentile
- sensor_rotation_vec_x_min
- sensor_rotation_vec_x_max
- sensor_rotation_vec_x_mean
- sensor_rotation_vec_x_quadratic_mean
- sensor_rotation_vec_x_25_percentile
- sensor_rotation_vec_x_50_percentile
- sensor_rotation_vec_x_75_percentile
- sensor_rotation_vec_x_100_percentile
- sensor_rotation_vec_y_min
- sensor_rotation_vec_y_max
- sensor_rotation_vec_y_mean
- sensor_rotation_vec_y_quadratic_mean
- sensor_rotation_vec_y_25_percentile
- sensor_rotation_vec_y_50_percentile
- sensor_rotation_vec_y_75_percentile
- sensor_rotation_vec_y_100_percentile
- sensor_rotation_vec_z_min
- sensor_rotation_vec_z_max
- sensor_rotation_vec_z_mean
- sensor_rotation_vec_z_quadratic_mean
- sensor_rotation_vec_z_25_percentile
- sensor_rotation_vec_z_50_percentile
- sensor_rotation_vec_z_75_percentile
- sensor_rotation_vec_z_100_percentile
- sensor_proximity_min
- sensor_proximity_max
- sensor_proximity_mean
- sensor_proximity_quadratic_mean
- sensor_proximity_25_percentile
- sensor_proximity_50_percentile
- sensor_proximity_75_percentile
- sensor_proximity_100_percentile

Multimedia
---

These features indicate if the user was using the smartphone's camera for taking a picture or recording a video.

- multimedia_picture
- multimedia_video

Label specified by the user
---

The situation (context) label specified by the user.

- label

# Related Publications

- **Lightweight Modeling of User ContextCombining Physical and Virtual Sensor Data**, Mattia Giovanni Campana, Dimitris Chatzopoulos, Franca Delmastro, Pan Hui. UBICOMP/CPD 2018, OCTOBER 8-12, 2018, SINGAPORE

